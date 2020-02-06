# Rpackages

#python server
python -m SimpleHTTPServer 8000

update.packages(repos="http://localhost:8000", ask=FALSE)

# R server
library(servr)
setwd("<cloned repo dir>")
servr::httd()
update.packages(repos="http://localhost:7826", ask=FALSE)


Required packages to build from source
-----------------


sudo apt update
sudo apt-get install build-essential
sudo apt install dirmngr gnupg apt-transport-https ca-certificates

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF

sudo sh -c 'echo "deb https://download.mono-project.com/repo/ubuntu stable-bionic/snapshots/5.20.1 main" > /etc/apt/sources.list.d/mono-official-stable.list'

sudo apt update
sudo apt install mono-complete 

This install command worked
---------------------------
R CMD INSTALL -l ~/repositories/R --build --no-build-vignettes .