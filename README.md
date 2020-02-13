# Restaurants-
Restaurants and markets in Los Angeles county are regularly inspected for health code violations. The county makes these data publicly available and accessible, enabling a transparent look into this public health information.

## Reading in the data and having a peek
library(tidyverse)

inspections <- read_csv("../input/inspections.csv")
violations <- read_csv("../input/violations.csv")

all <- inspections %>%
  inner_join(violations, by="serial_number")

glimpse(all)
