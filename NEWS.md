

## rtables 0.1.1

* `rtablulate` family of functions do not support the `row_*_data_args` arguments anymore. Instead, the `col_wise_args` argument is introduced.
* add functions `order_rrows`, `sort_rrows`, `order_rtables`, and `sort_rtables` are introduced.
* prevent `rtables` from being unlisted with `unlist.rtables`


## rtables 0.1.0.6

* `Viewer` now also accepts objects of class `shiny.tag` (defined in package `htmltools`)
* `as.html` accepts `class.table`, `class.tr`, `class.th`, and `class.td` as an argument

## rtables 0.1.0.5

* added `sprintf_format` for formatting rcells (thanks to Doug Kelkhoff for the suggestion)
* added `"(N=xx)"` and `">999.9"` format labels
* `rtabulate` has now an argument `col_N` and the function `col_N()`

## rtables 0.1.0

Version `0.1.0` is a major re-design with lots of internal refactoring and the
following API changes:

* Redesign: `rtable` has now `header` argument instead of `col.names`. A
`header` can be created with `rheader` and is a collection of `rrow`s. If
`header` is set to `c("A", "B")` then `rtable` will create the `rheader` with a
single `rrow`  and by setting `row.name` to `NULL`.

* `header` and `header<-` function added

* renamed `get_rcell_formats` to `list_rcell_format_labels`

* If `rcell` format is `NULL` then the cell content will be converted to a string with `paste(as.character(x), collapse = ', ')`

* accessor `[i,]` works now to subset a table.

* `rbind` method for rtables

* `row.names<-.rtable` method

* `rtabulate` added for creating tables

* `indented_row.names` function added


## rtables 0.0.1

* Initial public release