# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Semi-Parametric Quantile Regression Use SPQR With (In) R Software
install.packages("remotes")
remotes::install_github("stevengxu/SPQR")
library("SPQR")
SPQR = read.csv("https://raw.githubusercontent.com/timbulwidodostp/SPQR/main/SPQR/SPQR.csv",sep = ";")
# Estimation Semi-Parametric Quantile Regression Use SPQR With (In) R Software
X <- SPQR$X
Y <- SPQR$Y
control <- list(iter = 300, warmup = 200, thin = 1)
SPQR <- SPQR(X = X, Y = Y, method = "MCMC", control = control, normalize = TRUE, verbose = FALSE)
print(SPQR, showModel = TRUE)
plotEstimator(SPQR, type = "PDF", X = 0, ci.level = 0.95)
# Semi-Parametric Quantile Regression Use SPQR With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished