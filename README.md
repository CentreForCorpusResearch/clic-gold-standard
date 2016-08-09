
# clic-gold-standard

This is a manually curated gold standard for quote extraction in literary texts.

It contains a number of randomly selected paragraphs from
15 novels by Charles Dickens and 29 non-Dickensian 19th century
novels.

The files are XML files. Quotes are highlighted with `<qs/>`, `<qe/>`, `<alt-qs/>`,
`<alt-qe/>` milestones, respectively shorthand for "quote start", "quote end",
"alternative quote start", and "alternative quote end".


# Remarks

The difference between `<qs/> or <qe/>` tags and `<alt-qs/> or <alt-qe/>` tags has not
been manually verified. This means that a tag can mistakenly be identified as an
alternative quote even if it is a normal quote. For computing precision and recall
this is not an issue if one wants to measure whether quotes (regardless of whether
  they are alternative) are retrieved.

The gold standard is also annotates suspensions between alternative quotes.

# Known issues

- 19C quotes, sample 1, vanity.c13.p67, sample num 3, has a single quotation mark which should not be there, https://books.google.be/books?id=tQkoAAAAMAAJ&pg=PA64&dq=My+chief+clerk,+Mr.+Chopper&hl=en&sa=X&ved=0ahUKEwiw_qPKx_HJAhWLfxoKHdLzBMAQ6AEIJTAB#v=onepage&q=My%20chief%20clerk%2C%20Mr.%20Chopper&f=false

- 19C quotes, sample 1, NorthS.c14.p10: an alternative quote, but with the same quotation marks (`'  ' '  '`), we have added `<alt-qs/>` and `<alt-qe/>` tags but it is admittedly ambiguous, cf. https://books.google.be/books?id=zlIbAgAAQBAJ&pg=PT993&dq=my+father+may+rely+upon+me,+++++++++++++++++that+I+will+bear+with+all+proper+patience&hl=en&sa=X&ved=0ahUKEwjV96PGn_DJAhUHlR4KHXIsDDkQ6AEIHzAA#v=onepage&q=my%20father%20may%20rely%20upon%20me%2C%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20that%20I%20will%20bear%20with%20all%20proper%20patience&f=false

- 19C quotes, sample 3, sample3.c74.s1, wh.c30.s94: contains a closing double quotation mark, but not an opening one (`Dunnot say I wanted it, but ask of yourseln."`)

- 19C quotes, sample 3, sample3.c99.p45, arma.c38.p37, sample3.c99.s165 contains a triple alternative quote

- 19C quotes, sample 4, arma.c39.s774, sample num 70 contains a double quotation mark where one would expect a single quotation mark

- 19C quotes, sample 4, frank.c16.p9: an alternative quote, but the gold standard does not mark it up and does not contain the other parts of the quote

- 19C quotes, sample 4, native.c27.p18, sample num 39: uses both single and double quotation marks for the same quote

- 19C quotes, sample 2, sample2.c39.s2 (cf. also 19C quotes sample2.c83.s3 and sample3.c99.s462): contains two alternative quotes, that are not really quotes and hence it is marked up as a suspensions, though that is debatable: `<s sid="2" id="sample2.c39.s2"><qs/>"He hit you hard with the <alt-qs/>'dissecting-knife,'<alt-qe/>
                <sls/>doctor; and now you have hit him back again with your <sle/><alt-qs/>'natural explanation.'<alt-qe/>
                </s>`

# Recently solved issues

- 19C quotes, sample 1, sample1.c81.s1: an extended quote, but is not marked as one. (This might be an inconsistency in the Armadale, cf. https://books.google.be/books?id=gpNEAQAAMAAJ&pg=PA199&lpg=PA199&dq=Pray+excuse+my+troubling+you,+before+you+go&source=bl&ots=73DyF7COoW&sig=dxI--amHsfs8UyE0JYyyFjVhxKE&hl=en&sa=X&ved=0ahUKEwjx-8CxnvDJAhXL2R4KHXpADRQQ6AEIHzAA#v=onepage&q=Pray%20excuse%20my%20troubling%20you%2C%20before%20you%20go&f=false)

- 19C quotes, sample 2, sample2.c14.s1: this is correctly annotated as an extended quote, but it does not have the XML attributes for extended quotes (beginning, middle, end)

- 19C quotes, sample 3, sample3.c74.s1: an alternative quote, but the gold standard does not mark it up and does not contain the other parts of the quote

- 19C quotes, sample 3, sample3.c99.s1, arma.c38.p37: an alternative quote, but the gold standard does not mark it up and does not contain the other parts of the quote

- 19C quotes, sample 3, arma.c38.p37, sample num 99 is an extended quote, but the gold standard does not mark it up and does not contain the other parts of the quote

- 19C quotes, sample 4, samples from Frankenstein start with single backticks rather than single quotation marks. These backticks have been replaced in the latest Frankenstein Gutenberg file

- 19C quotes, sample 4, arma.c39.p170, sample num 70 is an extended quote, but the gold standard does not mark it up and does not contain the other parts of the quote

# To do

- add definitions
