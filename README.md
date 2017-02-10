# For-loop-in-R
<55>
For Loop in R
for (val in sequence)
{
    statement
}


************************* Example *********************************************************************
x <- c(2,5,3,9,8,11,6)
count <- 0
for (val in x) 
{
    if(val %% 2 == 0)  count = count+1
}
print(count)
