# R_save_plot_to_file

It's best to have the plot save to a file within your code, so you don't have to GUI click to get your 
plots into eps or pdf format

```R
plot.to.file = 1  # Set to 0 if you're just testing how the plot looks in R.
outdir.figs = "C:/directory/mythesis/figures/"  # Directory where to put the figures

if (plot.to.file == 1){
  setwd(outdir.figs)
  postscript("fig_xx_filename.eps")
  }
  
par(oma=c(2,0,0,0))  # Other parameters as needed
plot(xx.....)  # all plot and legend commands

if (plot.to.file == 1){
dev.off()
}

  
