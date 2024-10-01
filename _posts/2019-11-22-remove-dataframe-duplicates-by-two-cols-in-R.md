---
title: 'Removing dataframe duplicates by two cols'
date: 2019-11-22
permalink: /posts/2019/11/Removing_dataframe_duplicates/
tags:
  - RLanguage
  - Programming
  - NA
---

This R code solves the problem of removing duplicates in a dataframe, by comparing the unordered values of two columns. 

The **dplyr** package is used.


{% highlight r %}
if(!require(dplyr, quietly = TRUE, warn.conflicts = FALSE)){
  install.packages("dplyr", quiet = TRUE)
  require(dplyr, quietly = TRUE, warn.conflicts = FALSE)
}


# a small dataset
df_test <- data.frame(col_a = letters[c(1,2,3,3)], col_b = letters[c(2,1,3,3)], len = 1:4, stringsAsFactors = F)
print(df_test)
{% endhighlight %}



{% highlight text %}
##   col_a col_b len
## 1     a     b   1
## 2     b     a   2
## 3     c     c   3
## 4     c     c   4
{% endhighlight %}



{% highlight r %}
# create two new columns, remove duplicates, and then remove the two columns
df_test_unique <- df_test %>%
  rowwise() %>%
  distinct(maxID = max(col_a, col_b), minID = min(col_a, col_b), .keep_all = T) %>%
  select(-c(maxID, minID)) %>%
  ungroup()

# after removing duplicates
print(df_test_unique)
{% endhighlight %}



{% highlight text %}
## # A tibble: 2 x 3
##   col_a col_b   len
##   <chr> <chr> <int>
## 1 a     b         1
## 2 c     c         3
{% endhighlight %}
