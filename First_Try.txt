
#Reading the data from the files
BBSHP <- read.csv("D:/Documents/As/Data-Minning/data/BBSHP.csv")
View(BBSHP)
GDP <- read.csv("D:/Documents/As/Data-Minning/data/GDP.csv")
View(GDP)
GDP <- read.csv("D:/Documents/As/Data-Minning/data/GDP.csv")
View(GDP)
IMR <- read.csv("D:/Documents/As/Data-Minning/data/IMR.csv")
View(IMR)
PCGEOH <- read.csv("D:/Documents/As/Data-Minning/data/PCGEOH.csv")
View(PCGEOH)

#Merging the data based on the common Variables "Country" and "Year".
mydata <- merge(BBSHP, GDP, by=c("Country","Year"), all=TRUE)
mydata
mydata <- merge(BBSHP, GDP, by=c("Country","Year"))
mydata
mydata$GDP<-NULL
mydata
mydata <- merge(mydata, IMR, by=c("Country","Year"))
mydata <- merge(mydata, PCGEOH, by=c("Country","Year"))
mydata
mydata$Country<-NULL
mydata
results<-kmeans(mydata, 5)
mydata<-na.omit(mydata)
results<-kmeans(mydata, 5)
results

#Plotting graphs - Comparing 2 components againsts each other one at a time still using K means

plot(mydata[c("GDP.in.Billion.Dollars", "IMR")], col= results$cluster)
plot(mydata[c("Year", "IMR")], col= results$cluster)
plot(mydata[c("BBSHP.in...", "IMR")], col= results$cluster)
plot(mydata[c("PCGEOH", "IMR")], col= results$cluster)

#Plotting graphs - Comparing all conponents of the table against each other all in one k-mmeans cluster graph
set.seed(5)
x=matrix(rnorm(mydata), ncol=5)
head(x)
x=matrix(rnorm(681*5), ncol=5)
head(x)
km.out=kmeans(x,5,nstart=20)
km.out$cluster
plot(mydata,col=(km.out$cluster+1),main="relationship between income and health status of countries and the infant mortality rate",pch=20,cex=2)
plot(x,col=(km.out$cluster+1),main="relationship between income and health status of countries and the infant mortality rate",pch=20,cex=2)

#STARTING HEIRARCHICAL CLUSTERING###
hc.complete=hclust(dist(mydata),method="complete")
hc.single=hclust(dist(mydata),method="single")
plot(hc.complete,main="Hierarchical Clustering(Complete)",cex=0.9)
plot(hc.single,main="Hierarchical Clustering(Single)",cex=0.9)
