# Friendly Time Formats

Have you ever had to build a way too complicated time format?

```{r}
my_time_format = "%Ey/%b/%0d%t%0I:%0M:%0S3 %p %Z"
```

No human could read this. striptimer allows you to build understandable time formats.

```{r}
time_format(year %>% short %>% religious,
            "/",
            month %>% name %>% short,
            "/",
            day %>% roman,
            
            tab,
            
            hour %>% twelve %>% roman,
            ":",
            minute %>% roman,
            ":",
            second %>% digits(3),
            " ",
            am_pm,
            " ",
            timezone %>% name)
```

Inspired by kevinushey/rex

# Installation

```{r}
library(devtools)
install_github("bramtayl/strptimer")
```
