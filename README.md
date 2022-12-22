# Stanford Harmful Language Initiative Dataset

**Content Warning: This page contains language that is offensive or harmful. Please engage with this page at your own pace.**

This repository contains tabulated data from Stanford's [Elimination of Harmful Language Initiative](https://itcommunity.stanford.edu/news/introducing-elimination-harmful-language-initiative-website), extracted from a [December 19, 2022 snapshot](http://web.archive.org/web/20221219160303/https://itcommunity.stanford.edu/ehli) of the site.

## Dataset

The dataset can be accessed [here](Stanford_harmful_language_dataset.csv). A sample of the data is shown below:

| Category | Instead of  | Consider using                       | Context                                                                                                       |
|----------|-------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Ableist  | addict      | person with a substance use disorder | Using person-first language helps to not define people by just one of their characteristics.                  |
| Ableist  | addicted    | hooked                               | Trivializes the experiences of people who deal with substance abuse issues.                                   |
| Ableist  | addicted    | devoted                              | Trivializes the experiences of people who deal with substance abuse issues.                                   |
| Ableist  | basket case | nervous                              | Originally referred to one who has lost all four limbs and therefore needed to be carried around in a basket. |

As shown above, the "Instead of" column can contain repeated values - the word "addicted" shows up twice because it may be replaced with the words "hooked" or "devoted".

Similarly, the "Consider using" column may contain repeated values; for example in the following snippet, the word "hooray" can be used as a replacement for either "hip-hip hurray" or "hip hip hooray".

| Category                  | Instead of     | Consider using | Context                                                                                                                                                    |
|---------------------------|----------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Additional Considerations | hip-hip hurray | hooray         | This term was used by German citizens during the Holocaust as a rallying cry when they would hunt down Jewish citizens living in segregated neighborhoods. |
| Additional Considerations | hip hip hooray | hooray         | This term was used by German citizens during the Holocaust as a rallying cry when they would hunt down Jewish citizens living in segregated neighborhoods. |

Raw data extracted from the site can be found in the [raw/](raw/raw.csv) folder.

## Contributing

The dataset was generated by extracting the raw data using the Table Capture plugin for Chrome, passing it into Pandas, and expanding many-to-one relationships into one-to-one relationships (e.g. expanding "addicted" -> "hooked/devoted" into "addicted" -> "hooked" and "addicted" -> "devoted"). Some of the data may not have been extracted/reformatted properly, or could be expanded further. If you find this is the case, please [submit a pull request](https://github.com/naveenarun/StanfordHarmfulLanguage/pulls) to revise the table.
