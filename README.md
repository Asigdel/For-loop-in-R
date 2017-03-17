# For-loop-in-R
To cat data

```
datab<-data.frame()
str(test1)
test1$TD1f<-as.character(test1$TD1)
for (i in 1:49){
  for (k in 5:24){
    col1<-test1[i,k]
    col2<-test1[i,k+20]
    temp[[k]]<-c(data.frame(col1,col2))
    print(temp[[k]])
    datab<-rbind(datab,temp[[k]])
    #print(data.frame(col1, col2) )
  }
}
print(datab)
datab$Date<-as.Date.numeric(datab$col1, origin="1970-01-01")
View(datab)
```

# Dev_dai-llop-in-R

test1$TD1f<-as.character(test1$TD1)
for (i in 2:49){ 
  testn<- test1[i,]
  testn2 <- testn[!is.na(testn)]
  lengthn<- length(testn2)/2
  if(lengthn > 5){
    for (k in 5:10){
    col_herd<-test1[i,1]
    col_cow<-test1[i,2]
    col_ld<-test1[i,3]
    col_cd<-test1[i,4]
    col_date<- test1[i,k]
    col_dm<- test1[i,k+20]
    temp[[k]] <- c(data.frame(col_herd, col_cow, col_ld, col_cd,col_date, col_dm))
    print(temp[[k]])
    datab<-rbind(datab,temp[[k]])
    #print(datab)
    #print(data.frame(col1, col2) )
  }
  }
}
print(datab)
datab$Date<-as.Date.numeric(datab$col_date, origin="1970-01-01")
View(datab)
write.csv(datab, file="Depthoutput.txt", col.names=FALSE,row.names=FALSE) #Filename is .txt to avoid confusions in reading files from same folder
rm(datab)
colnames(test1)
library(dplyr)
grouped <- group_by(test1, c)


attach(mtcars)
aggdata <-aggregate(mtcars, by=list(cyl,vs), 
                    FUN=mean, na.rm=TRUE)
print(aggdata)
