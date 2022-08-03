rm(list=ls())

library(pdftools)
library(stringr)

# inputs
infile <- "Path for the pdf"  # input pdf
prefix <- "KABC"  # output pdf's will begin with this prefix

num <- pdf_length(infile)
st <- seq(1, num, 5)
en <- pmin(st + 4, num)

for (i in seq_along(st)) {
  outfile <- sprintf("%s%0*d.pdf", prefix, nchar(num), i)
  pdf_subset(infile, pages = st[i]:en[i], output = outfile)
}