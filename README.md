# Datasets

This repo contains datasets that I collected for the projects of the small scale. All of them seem interesting to investigate for me but I have not done anything specific with them - some vizualisations or modelling at best.

By launching it, I aim to motivate myself to work on something at least once in a while to maintain the skills of data collection & preparation.

# Descriptions

### `most_published_authors_in_russia.csv`

The data is in Russian.

The original data comes from [here](https://www.bookchamber.ru/statistics.html). The **Accounts Chamber of Russian Federation** collects data about the volumes of printed products in Russia annually in aggregated format in .doc or .pdf files. They calculate the measures for the regions of Russia, registered printing houses, certain themes, types of products, and so on. I have extracted the tables about **the most printed authors in each of the given years (2012-2021)**.

My purpose was to reveal the dramatic change in book consumption that happened in the last few years. The data shows how the dominance of Darya Dontsova (most known for the dozes if not the hundreds of detective stories) was destroyed by the group of both classic and contemporary authors, most notably Steven King (in the first six months of 2022, the year not included in the data, [there were over a million of his books printed in Russia](https://daily.afisha.ru/news/66146-stiven-king-stal-samym-izdavaemym-v-rossii-avtorom-2022-goda/)).

The data size is 400 observations of 7 variables. The list of variables in the suggested subset includes:
  - The `surname` of the author who got to the top-20 printed authors in a given year,
  - `n_units`, i.e. number of books' titles released in a given year related to the respective author,
  - `overall_circulation`, that is, the total circulation of the author's book printed in a given year,
  - `type` is a categorical variable ("authors" or "children") that represents the categories distinguished by the Accounts Chamber of Russian Federation (it classifies the authors to those who are *just* authors and those who wrote for the children),
  - `year` of calculations,
  - `printed_sheets` is the Russian unit of measurement for the printed text (*печатный лист-оттиск*),
  - `full_name` is the full name of the respective author.
  
 
 ### `movies_izhevsk.csv`

The data is in Russian.
 
This file contains the data about the movies shown at the cinema club in Izhevsk, Russia, for app. the last 15 years. Cinema club was started back in 1970s and was called **Mirror** in honor of Tarkovsky's movie. The data was gathered from the [club's website](http://kinohorosho.ru/). My initial goal was to create a tool to search for the movies featured during the meetings. The result can be found in this [not-that-profficient-tableau viz](https://public.tableau.com/app/profile/arthur5379/viz/cinemaclubinIzhevskRussia/cinemaclub). I worked with this tool long ago as a first-year BA sociology student and struggled much to adjust its sizes - so, I guess, this data can be given to the tableau beginners for them to become better then me.

The data size is 912 observations of 11 variables. The list of variables includes:
  - `russian_name` and `foreign_name`, the movie title given in two languages (if present in website descriptions) respectively,
  - `href`, i.e. the link to the film announcement,
  - `director`, given in Russian,
  - `country`, given in Russian, that can include multiple countries through "-",
  - `country2`, that signifies whether a movie was produced by multiple countries,
  - `year` of creation,
  - `duration` in minutes,
  - `duration2`, that indicates if the movie is shorter than 50 minutes,
  - `announced_name`, movie name as announced,
  - `announced_features`, features as announced.


### `letters_not_about_love.csv`

The data is in Russian.

The file contains the ready-to-use version of the short epistolary novel called [**"Zoo, or Letter not about Love"** (1922)](https://www.goodreads.com/book/show/27717055-zoo--of-brieven-niet-over-liefde) and written by Viktor Shklovsky. The text was taken from [here](http://marie-olshansky.ru/ct/zoo.shtml]). The book itself consists of observations Shklovsky did while living in Berlin during his emigrant period. It is also touching that the storytelling is based on the (partially fictional) correspondence between the author and Elsa Triolet, the woman he loved (the portraits may be found in this [NYT note](https://www.nytimes.com/2021/02/13/books/review/zoo-viktor-shklovsky-elsa-triolet-letters-not-about-love.html)). She asks the main character aka Viktor not to write her about love - and he accepts the challenge, abusing all kinds of metaphors and stylistic tricks. Besides the novel itself being a great opportunity to cry in bed, it is also a challenge for sentiment analysts due to Shklovsky's style! I mainly used this data for this exact purpose.

The data size is 103 observations of 4 variables. The list of variables includes:
  - `text`, the novel's text itself, including foreword, epigraph, dedication, letters' titles, prefaces to letters, and letters,
  - `text_part`, indicates the type of the `text` be that dedication, foreword, epigraph, letter summary (written by Viktor), or the letter itself, 
  - `chapter`, indicates the order of a letter (1-30, `NA` for not chapter-related pieces),
  - `author`, that can be Viktor Shklovsky, Elsa Triolet, or Velimir Khlebnikov (whose text was used as an epigraph).
