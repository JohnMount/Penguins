Penguins
================

[https://github.com/allisonhorst/palmerpenguins Palmer Penguins
example](https://github.com/allisonhorst/palmerpenguins) as comma
separated value files.

``` r
penguins <- read.table(
  'https://raw.githubusercontent.com/JohnMount/Penguins/main/penguins.csv', 
  header = TRUE, 
  sep = ',', 
  quote = '"')

print(dim(penguins))
```

    ## [1] 344   7

``` r
knitr::kable(head(penguins))
```

| species | island    | bill\_length\_mm | bill\_depth\_mm | flipper\_length\_mm | body\_mass\_g | sex    |
| :------ | :-------- | ---------------: | --------------: | ------------------: | ------------: | :----- |
| Adelie  | Torgersen |             39.1 |            18.7 |                 181 |          3750 | male   |
| Adelie  | Torgersen |             39.5 |            17.4 |                 186 |          3800 | female |
| Adelie  | Torgersen |             40.3 |            18.0 |                 195 |          3250 | female |
| Adelie  | Torgersen |               NA |              NA |                  NA |            NA | NA     |
| Adelie  | Torgersen |             36.7 |            19.3 |                 193 |          3450 | female |
| Adelie  | Torgersen |             39.3 |            20.6 |                 190 |          3650 | male   |

``` r
penguins_raw <- read.table(
  'https://raw.githubusercontent.com/JohnMount/Penguins/main/penguins_raw.csv', 
  header = TRUE, 
  sep = ',', 
  quote = '"')

print(dim(penguins_raw))
```

    ## [1] 344  17

``` r
knitr::kable(head(penguins_raw))
```

| studyName | Sample.Number | Species                             | Region | Island    | Stage              | Individual.ID | Clutch.Completion | Date.Egg   | Culmen.Length..mm. | Culmen.Depth..mm. | Flipper.Length..mm. | Body.Mass..g. | Sex    | Delta.15.N..o.oo. | Delta.13.C..o.oo. | Comments                       |
| :-------- | ------------: | :---------------------------------- | :----- | :-------- | :----------------- | :------------ | :---------------- | :--------- | -----------------: | ----------------: | ------------------: | ------------: | :----- | ----------------: | ----------------: | :----------------------------- |
| PAL0708   |             1 | Adelie Penguin (Pygoscelis adeliae) | Anvers | Torgersen | Adult, 1 Egg Stage | N1A1          | Yes               | 2007-11-11 |               39.1 |              18.7 |                 181 |          3750 | MALE   |                NA |                NA | Not enough blood for isotopes. |
| PAL0708   |             2 | Adelie Penguin (Pygoscelis adeliae) | Anvers | Torgersen | Adult, 1 Egg Stage | N1A2          | Yes               | 2007-11-11 |               39.5 |              17.4 |                 186 |          3800 | FEMALE |           8.94956 |        \-24.69454 | NA                             |
| PAL0708   |             3 | Adelie Penguin (Pygoscelis adeliae) | Anvers | Torgersen | Adult, 1 Egg Stage | N2A1          | Yes               | 2007-11-16 |               40.3 |              18.0 |                 195 |          3250 | FEMALE |           8.36821 |        \-25.33302 | NA                             |
| PAL0708   |             4 | Adelie Penguin (Pygoscelis adeliae) | Anvers | Torgersen | Adult, 1 Egg Stage | N2A2          | Yes               | 2007-11-16 |                 NA |                NA |                  NA |            NA | NA     |                NA |                NA | Adult not sampled.             |
| PAL0708   |             5 | Adelie Penguin (Pygoscelis adeliae) | Anvers | Torgersen | Adult, 1 Egg Stage | N3A1          | Yes               | 2007-11-16 |               36.7 |              19.3 |                 193 |          3450 | FEMALE |           8.76651 |        \-25.32426 | NA                             |
| PAL0708   |             6 | Adelie Penguin (Pygoscelis adeliae) | Anvers | Torgersen | Adult, 1 Egg Stage | N3A2          | Yes               | 2007-11-16 |               39.3 |              20.6 |                 190 |          3650 | MALE   |           8.66496 |        \-25.29805 | NA                             |

Palmer Penguins data from:

<https://github.com/allisonhorst/palmerpenguins>

> citation(“palmerpenguins”)
> 
> To cite palmerpenguins in publications use:
> 
> Gorman KB, Williams TD, Fraser WR (2014) Ecological Sexual Dimorphism
> and Environmental Variability within a Community of Antarctic Penguins
> (Genus Pygoscelis). PLoS ONE 9(3): e90081.
> <https://doi.org/10.1371/journal.pone.0090081>
> 
> A BibTeX entry for LaTeX users is
> 
> @Article{, title = {Ecological Sexual Dimorphism and Environmental
> Variability within a Community of Antarctic Penguins (Genus
> Pygoscelis)}, author = {Gorman KB and Williams TD and Fraser WR},
> journal = {PLoS ONE}, year = {2014}, volume = {9(3)}, number =
> {e90081}, pages = {-13}, url =
> {<https://doi.org/10.1371/journal.pone.0090081>}, }

Saved using `R`:

    # install.packages("remotes")
    remotes::install_github("allisonhorst/palmerpenguins")
    write.csv(penguins, 'penguins.csv', row.names = FALSE, quote = FALSE)
    write.csv(penguins_raw, 'penguins_raw.csv', row.names = FALSE, quote = TRUE)

Exported so Python users can also use this data (original package
doesn’t seem to currently export a csv).

This page found here: <https://github.com/JohnMount/Penguins>

Python example here:
<https://github.com/JohnMount/Penguins/blob/main/Penguins.ipynb>
