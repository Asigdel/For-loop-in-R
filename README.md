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

