# Rpackages
install.packages("rClr", repos = paste("file:", normalizePath(getwd(), winslash = "/"), sep = ""), type = "win.binary")

tools::write_PACKAGES("bin/windows/contrib/3.4/.", type="win.binary")

