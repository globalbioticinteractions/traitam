####################TRAITAM SPORE METRICS CALCULATIONS####################

# Loading packages
rm(list = ls())
library(tidyverse)
library(readxl)
library(picante)
library(phytools)
library(phylolm)
library(tidytree)
library(nlme)
library(ape)

# Loading data
setwd("C:/Users/liamn/OneDrive/Documentos/TraitAM") # NOTE: Modify for home directory
Liam_copy <- read.csv("DataRecord_2_TraitAMraw_18Jun2024.csv")

# Housekeeping
# Making sure data is recognized as numeric
Liam_copy[, grep("dim|wall_thick|color_most|orn_height_mean", names(Liam_copy))] <- lapply(Liam_copy[, grep("dim|wall_thick|color_most|orn_height_mean", names(Liam_copy))], as.numeric)

#### Calculating the polar and equatorial axes
# Equatorial axis
Liam_copy$equatorial_mean <- NA
Liam_copy$equatorial_min <- NA
Liam_copy$equatorial_max <- NA
op1 <- which(
  ((as.numeric(Liam_copy$dim1.min) + as.numeric(Liam_copy$dim1.max))/2) <=
    ((as.numeric(Liam_copy$dim2.min) + as.numeric(Liam_copy$dim2.max))/2))

Liam_copy$equatorial_min[op1] <- 
  (as.numeric(Liam_copy$dim1.min2[op1]))

Liam_copy$equatorial_mean[op1] <- 
  ((as.numeric(Liam_copy$dim1.min[op1]) + as.numeric(Liam_copy$dim1.max[op1]))/2)

Liam_copy$equatorial_max[op1] <- 
  (as.numeric(Liam_copy$dim1.max2[op1]))

op2 <- which(
  ((as.numeric(Liam_copy$dim1.min) + as.numeric(Liam_copy$dim1.max))/2) >
    ((as.numeric(Liam_copy$dim2.min) + as.numeric(Liam_copy$dim2.max))/2))

Liam_copy$equatorial_min[op2] <- 
  (as.numeric(Liam_copy$dim2.min[op2]))

Liam_copy$equatorial_mean[op2] <- 
  ((as.numeric(Liam_copy$dim2.min[op2]) + as.numeric(Liam_copy$dim2.max[op2]))/2)

Liam_copy$equatorial_max[op2] <- 
  as.numeric(Liam_copy$dim2.max[op2])

# Polar axis
Liam_copy$polar_mean <- NA
Liam_copy$polar_min <- NA
Liam_copy$polar_max <- NA
op1 <- which(
  ((as.numeric(Liam_copy$dim1.min) + as.numeric(Liam_copy$dim1.max))/2) >
    ((as.numeric(Liam_copy$dim2.min) + as.numeric(Liam_copy$dim2.max))/2))

Liam_copy$polar_min[op1] <- 
  (as.numeric(Liam_copy$dim1.min2[op1]))

Liam_copy$polar_mean[op1] <- 
  ((as.numeric(Liam_copy$dim1.min[op1]) + as.numeric(Liam_copy$dim1.max[op1]))/2)

Liam_copy$polar_max[op1] <- 
  (as.numeric(Liam_copy$dim1.max2[op1]))

op2 <- which(
  ((as.numeric(Liam_copy$dim2.min) + as.numeric(Liam_copy$dim2.max))/2)>=
    ((as.numeric(Liam_copy$dim1.min) + as.numeric(Liam_copy$dim1.max))/2))

Liam_copy$polar_min[op2] <- 
  (as.numeric(Liam_copy$dim2.min[op2]))

Liam_copy$polar_mean[op2] <- 
  ((as.numeric(Liam_copy$dim2.min[op2]) + as.numeric(Liam_copy$dim2.max[op2]))/2)

Liam_copy$polar_max[op2] <- 
  as.numeric(Liam_copy$dim2.max[op2])

Liam_copy[, grep("equat|polar", names(Liam_copy))] <-
  lapply(Liam_copy[, grep("equat|polar", names(Liam_copy))], as.numeric)

#### Calculating Volume, Wall Investment, and Shape
# Just having a copy 
Liam_copy_org <- Liam_copy

# Adding volumes
Liam_copy <-
  left_join(
    left_join(
      Liam_copy %>% 
        select(c("good.names", "equatorial_min", "equatorial_mean", "equatorial_max")) %>% 
        pivot_longer(c("equatorial_min", "equatorial_mean", "equatorial_max"),
                     names_to = "equatorial_type",values_to = "equatorial"),
      
      Liam_copy %>% 
        select(c("good.names", "polar_min", "polar_mean", "polar_max")) %>% 
        pivot_longer(c("polar_min", "polar_mean", "polar_max"),
                     names_to = "polar_type", values_to = "polar")
    ),
    
    Liam_copy %>% 
      select(c("good.names", "min_wall_thickness", "mean_wall_thickness", "max_wall_thickness")) %>% 
      pivot_longer(c("min_wall_thickness", "mean_wall_thickness", "max_wall_thickness"),
                   names_to = "wall_type", values_to = "wall")
  )

# Removing some entries that are not prolate spheroids
m <- which(Liam_copy$polar < Liam_copy$equatorial)

Liam_copy <- Liam_copy[-m, ]

# Calculating total spore volume
Liam_copy$total_volume <- (Liam_copy$equatorial^2)*Liam_copy$polar*(pi/6)

# Calculating the inner volume (i.e. the total volume minus the wall)
Liam_copy$inner_volume <- ((Liam_copy$equatorial-(2*Liam_copy$wall))^2)*(Liam_copy$polar-(2*Liam_copy$wall))*(pi/6)

# Calculating the shell volume (i.e. only the volume that represents the cell wall)
Liam_copy$shell_volume <- Liam_copy$total_volume-Liam_copy$inner_volume

# Calculating the Wall Investment
Liam_copy$investment <- Liam_copy$shell_volume/Liam_copy$total_volume

# Calculating the Shape as the aspect ratio
Liam_copy$shape <- Liam_copy$equatorial/Liam_copy$polar

Liam_copy_shell <- 
  left_join(
    Liam_copy %>% 
      group_by(good.names) %>% 
      summarise(shape_min = min(shape, na.rm = T),
                shape_median = median(shape, na.rm = T),
                shape_max = max(shape, na.rm = T),
                vol_min = min(total_volume, na.rm = T),
                vol_mean = mean(total_volume, na.rm = T),
                vol_max = max(total_volume, na.rm = T)),
    
    Liam_copy %>% 
      group_by(good.names) %>% 
      summarise(shell_vol_min = min(shell_volume, na.rm = T),
                shell_vol_mean = mean(shell_volume, na.rm = T),
                shell_vol_max = max(shell_volume, na.rm = T),
                investment_min = min(investment, na.rm = T),
                investment_mean = mean(investment, na.rm = T),
                investment_max = max(investment, na.rm = T)))

#### Adding back the data on the remaining traits we are using in the analysis: ornamentation, color and taxonomy
Liam_copy <- left_join(Liam_copy_org[, c("good.names", "orn_height_mean", "color_most", 
                                         "genus", "family", "order")],
                       Liam_copy_shell)

#### Saving as DataRecord_1
write.csv(
  Liam_copy[, c("good.names", "genus", "family", "order",
                "vol_mean", "shape_median", "color_most",
                "investment_mean", "orn_height_mean")],
  "DataRecord_1_CalculatedTraitMetrics_18Jun2024.csv", row.names = F)
