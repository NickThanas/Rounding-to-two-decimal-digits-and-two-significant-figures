##Rounding results to no more than two decimal places
##and no more than two significant figures

my_round <- function(x1) {
        x2 <- formatC(x1, digits=2, format="f", drop0trailing=FALSE)
        x2 <- as.numeric(x2)
        if(x2<100) {
                x3 <- formatC(x2, digits=2, format="fg", flag="#")
                x3 <- as.numeric(x3)
        }        
        else {
                x3 <- signif(x2, digits=2)
        }
        print(x3)
}
