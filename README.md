pollmean <- function("/Users/saira/coursera",pollutant,ID 1:332)
  Error: unexpected symbol in:
  "##sets the working directory by creating a path and creating one ## statement
pollmean"
> {
  +     data = numeric()
  +     for (i in id) {
    +         
      +         newRead = read.csv(paste(directory, "/", 
                                         +                                  formatC(i, width = 3, flag = "0"),".csv", sep = ""))
      +         
        +         data = c(data, newRead[[pollutant]])
        +     }
  +     return(mean(data, na.rm = TRUE))
  + }
## okay so now it's saying that "i for id" is the issue and I don't get it