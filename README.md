pollmean<-function(directory,pollutant,ID=1:332) 
{
data = numeric()
  for (i in ID) {
        newRead = read.csv(paste(directory, "/", 
        formatC(i, width = 3, flag = "0"),".csv", sep = ""))

         data = c(data, newRead[[pollutant]])  
         }
            return(mean(data, na.rm = TRUE))
            }
    

pollmean("specdata","sulfate",1:10)

complete<-function(directory,ID=1:332)
{
data=numeric()
  newRead=read.csv(paste(directory,"/",
      format(i,width = 3, flag = "0"), ".csv", sep = ""))

        data=c(data)
