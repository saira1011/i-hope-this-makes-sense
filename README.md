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
    nobs = numeric()
    for (i in ID) {
        newRead = read.csv(paste(directory, "/", 
        formatC(i, width = 3, flag = "0"),".csv", sep = ""))
         
         nobs=c(nobs,nrow(na.omit(newRead)))}
            return(data.frame(ID,nobs))
            }
    
complete("specdata",1)

corr<-function(directory,threshold=0)
 {
    df = complete(directory)
    ids = df[df["nobs"] > threshold, ]$ID
    corrr = numeric()
    for (ids in ID) {

        newRead = read.csv(paste(directory, "/", formatC(i, width = 3, flag = "0"), ".csv", sep = ""))
        dff = newRead[complete.cases(newRead), ]
        corrr = c(corrr, cor(df$sulfate, df$nitrate))
    }
    return(corrr)
}


