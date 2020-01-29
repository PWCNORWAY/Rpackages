# Rpackages

#python server
python -m SimpleHTTPServer 8000

update.packages(repos="http://localhost:8000", ask=FALSE)

# R server
library(servr)
setwd("<cloned repo dir>")
servr::httd()
update.packages(repos="http://localhost:7826", ask=FALSE)