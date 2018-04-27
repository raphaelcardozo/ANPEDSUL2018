#########################################################################
#Autor: Raphael Demostenes Cardozo - Email: raphaeldemostenes@gmail.com
#Orientadora: Profa.  Dra. Gabriela Schneider
#Mestrando Em Educação - PPGE- PE - UFPR
#Título: A Infraestrutura Das Escolas Públicas Das Capitais Do Brasil: Um Olhar Sobre A Questão Da Acessibilidade
#Data Inicial: 07/01/2018
#Versão Final:27/04/2018
#########################################################################
#   SCRIPT DE IMPORTAÇÃO E TRATAMENTO DA BASE DE DADOS                             #
#########################################################################
rm(list = ls())
getwd()
setwd ("C://r//anped")
save.image(file="impbase.RData")
####################################
#Importando base escola do Censo 2014  ##
####################################
library(readr)
CENSO2014<- read.table("C://r//base//2014//DADOS//ESCOLAS//ESCOLAS.csv", header=TRUE, sep="|")
View(CENSO2014)
names(CENSO2014)
str(CENSO2014)
CENSOESCOLA2014 <- subset(CENSO2014, select = c(1,2,3,5,8,9,11,12,22,66,67))
names(CENSOESCOLA2014)
str(CENSOESCOLA2014)
#####################################
library(dplyr)
ESCOLASCAPITAIS2014<-CENSOESCOLA2014%>%filter(CENSOESCOLA2014$DESC_SITUACAO_FUNCIONAMENTO==1& CENSOESCOLA2014$ID_DEPENDENCIA_ADM!=4 &
                                                    CENSOESCOLA2014$ID_LOCAL_FUNC_PREDIO_ESCOLAR!=0 &( 
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2800308|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==1501402|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==3106200|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==1400100|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==5300108|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==5002704|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==5103403|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==4106902|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==4205407|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2304400|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==5208707|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2507507|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==1600303|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2704302|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==1302603|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2408102|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==1721000|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==4314902|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==1100205|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2611606|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==1200401|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==3304557|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2927408|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2111300|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==3550308|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==2211001|
                                                    CENSOESCOLA2014$FK_COD_MUNICIPIO==3205309))

######################################
table(ESCOLASCAPITAIS2014$FK_COD_MUNICIPIO)
write.table(table(ESCOLASCAPITAIS2014$FK_COD_MUNICIPIO), "esc2014.txt", sep=";", row.names = TRUE, col.names = TRUE, quote = FALSE)
#######################################
#CENSO 2017                                                    #
#######################################
library(readr)
CENSO2017<- read.table("C://r//base//2017//DADOS//ESCOLAS//ESCOLAS.csv", header=TRUE, sep="|")
View(CENSO2017)
str(CENSO2017)
names(CENSO2017)
CENSOESCOLA2017 <- subset(CENSO2017, select = c(1,2,3,5,11,12,14,15,27,76,77))
names(CENSOESCOLA2017)
str(CENSOESCOLA2017)
#######################################
library(dplyr)
ESCOLASCAPITAIS2017<-CENSOESCOLA2017%>%filter(CENSOESCOLA2017$TP_SITUACAO_FUNCIONAMENTO==1& CENSOESCOLA2017$TP_DEPENDENCIA!=4 &
                                                CENSO2017$IN_LOCAL_FUNC_PREDIO_ESCOLAR==1 & ( 
                                                  CENSOESCOLA2017$CO_MUNICIPIO==2800308|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==1501402|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==3106200|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==1400100|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==5300108|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==5002704|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==5103403|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==4106902|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==4205407|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2304400|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==5208707|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2507507|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==1600303|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2704302|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==1302603|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2408102|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==1721000|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==4314902|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==1100205|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2611606|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==1200401|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==3304557|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2927408|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2111300|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==3550308|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==2211001|
                                                    CENSOESCOLA2017$CO_MUNICIPIO==3205309))
######################################
table(ESCOLASCAPITAIS2017$CO_MUNICIPIO)
write.table(table(ESCOLASCAPITAIS2017$CO_MUNICIPIO), "esc2017.txt", sep=";", row.names = TRUE, col.names = TRUE, quote = FALSE)
######################################

###################################################################
#   SCRIPT DE MANIPULAÇÃO DA BASE DE DADOS E RELATÓRIOS               #
###################################################################
rm(CENSO2014)
rm(CENSO2017)
rm(CENSOESCOLA2014)
rm(CENSOESCOLA2017)
save.image(file="impbase.RData")
#Freq. escolas
ESC2014FREQ<-table(ESCOLASCAPITAIS2014$FK_COD_ESTADO, useNA ="ifany")
ESC2014FREQ
ESC2017FREQ<-table(ESCOLASCAPITAIS2017$CO_UF, useNA ="ifany")
ESC2017FREQ
n<-nrow(ESCOLASCAPITAIS2014)
n2<-nrow(ESCOLASCAPITAIS2017)
fr14<-sort(round((ESC2014FREQ/n)*100,2))
fr17<-sort(round((ESC2017FREQ/n2)*100,2))
fr14
fr17
frt<-cbind(fr14,fr17)
frt
colnames(frt)<-c("2014","2017")
boxplot(frt[,c(1,2)], col = "#009E73" )
#####
#UF#
#####
descuf<-c("11-RO","12-AC", "13-AM", "14-RR", "15-PA", "16-AP", "17-TO",
          "21-MA", "22-PI", "23-CE", "24-RN", "25-PB", "26-PE", "27-AL", "28-SE","29-BA", 
          "31-MG","32-ES", "33-RJ", "35-SP", 
          "41-PR", "42-SC", "43-RS", 
          "50-MS","51-MT","52-GO", "53-DF")
###########################################
names(ESC2014FREQ)<-descuf
names(ESC2017FREQ)<-descuf
fr14gf<-sort(round((ESC2014FREQ/n)*100,2), decreasing = FALSE)
fr14gf
fr17gf<-sort(round((ESC2017FREQ/n2)*100,2), decreasing = FALSE)
fr17gf
fr1417f<-rbind(fr14gf,fr17gf)
fr1417f
############################################
library(plotrix)
# Gerando o gráfico
t1<-data.frame(fr14gf)
t2<-data.frame(fr17gf)
Lab<-c(
"Palmas","Vitória", "Aracaju",
"Florianópolis",
"Boa Vista",
"Cuiabá",
"Porto Velho",
"Macapá",
"Maceió",
"Rio Branco",
"Natal",
"Campo Grande",
"João Pessoa",
"São Luís ",
"Porto Alegre", 
"Belém",
"Goiânia",
"Belo Horizonte",
"Fortaleza" ,
"Teresina",
"Recife",
"Curitiba", 
"Salvador",
"Brasília",
"Manaus",
"Rio de Janeiro",
"São Paulo")
#############################
par(mar=pyramid.plot(t1$Freq,t2$Freq,
                     main="",lxcol="sienna",rxcol="thistle4",
                     gap=2.5,show.values=T, labels=Lab, ndig = 2,
                     top.labels=c("2014","Capital","2017")))
##############################

#####################
#Grafico bar dep e local. #
#####################

table(ESCOLASCAPITAIS2014$FK_COD_MUNICIPIO, ESCOLASCAPITAIS2014$ID_LOCALIZACAO)
par(mfrow = c(1, 1)) # Janela com 2 linhas e 1 coluna
ESCOLASCAPITAIS2014$ID_LOCALIZACAO<-factor(ESCOLASCAPITAIS2014$ID_LOCALIZACAO, levels = c(1,2),
                                           labels = c("Urbano","Rural"))
ESCOLASCAPITAIS2017$TP_LOCALIZACAO<-factor(ESCOLASCAPITAIS2017$TP_LOCALIZACAO, levels = c(1,2),
                                           labels = c("Urbano","Rural"))

loc14<-table(ESCOLASCAPITAIS2014$ID_LOCALIZACAO)
loc17<-table(ESCOLASCAPITAIS2017$TP_LOCALIZACAO)
loc<-cbind(loc14,loc17)
loc
colnames(loc)<-c("2014","2017")
grafloca<-barplot(loc,legend.text=row.names(loc), args.legend=list(x = "topleft", bty="n"), 
                  ylim=c(0,17000), beside = TRUE)
text(grafloca,loc,col="black",pos=3, cex=0.7, paste(loc))

############################################

ESCOLASCAPITAIS2014$ID_DEPENDENCIA_ADM<-factor(ESCOLASCAPITAIS2014$ID_DEPENDENCIA_ADM, levels = c(1,2,3),
                                               labels = c("F","E","M"))
ESCOLASCAPITAIS2017$TP_DEPENDENCIA<-factor(ESCOLASCAPITAIS2017$TP_DEPENDENCIA, levels = c(1,2,3),
                                           labels = c("F","E","M"))
dep14<-table(ESCOLASCAPITAIS2014$ID_DEPENDENCIA_ADM)
dep17<-table(ESCOLASCAPITAIS2017$TP_DEPENDENCIA)
dep<-cbind(dep14,dep17)
dep
colnames(dep)<-c("2014","2017")
grafdep<-barplot(dep,legend.text=row.names(dep), args.legend=list(x = "topleft", bty="n"), 
                 ylim=c(0,17000), beside = TRUE)
text(grafdep,dep,col="black",pos=3, cex=0.7, paste(dep))

#################
#wcpne 2014 e 17##
#################

table(ESCOLASCAPITAIS2014$ID_SANITARIO_PNE)
frsanit<-(table(ESCOLASCAPITAIS2014$ID_SANITARIO_PNE)/n)*100
frsanit
pie(frsanit, labels = c("51,73%","48,27%"), col = c("red","green"))
table(ESCOLASCAPITAIS2017$IN_BANHEIRO_PNE)
frsanit17<-(table(ESCOLASCAPITAIS2017$IN_BANHEIRO_PNE)/n2)*100
frsanit17
pie(frsanit17, labels = c("42,98%","57,02%"), col = c("red","green"))

################
#deppne2014e17##
################

table(ESCOLASCAPITAIS2014$ID_DEPENDENCIAS_PNE)
frdepadeq<-(table(ESCOLASCAPITAIS2014$ID_DEPENDENCIAS_PNE)/n)*100
frdepadeq
pie(frdepadeq, labels = c("60%","40%"), col = c("red","green"))
table(ESCOLASCAPITAIS2017$IN_DEPENDENCIAS_PNE)
frdep17<-(table(ESCOLASCAPITAIS2017$IN_DEPENDENCIAS_PNE)/n2)*100
frdep17
pie(frdep17, labels = c("56,39%","43,61%"), col = c("red","green"))

#############################
#mapas comparativos-preparação##
#wc acess 2014                            ##
#############################

table(ESCOLASCAPITAIS2014$ID_SANITARIO_PNE)
semwc<-(table(ESCOLASCAPITAIS2014$FK_COD_ESTADO ,ESCOLASCAPITAIS2014$ID_SANITARIO_PNE))
table(ESCOLASCAPITAIS2014$FK_COD_ESTADO ,ESCOLASCAPITAIS2014$ID_SANITARIO_PNE)
semwc<-semwc[,1]
semwc
comwc<-(table(ESCOLASCAPITAIS2014$FK_COD_ESTADO ,ESCOLASCAPITAIS2014$ID_SANITARIO_PNE))
comwc<-comwc[,2]
comwc
totalwc<-semwc+comwc
totalwc
total<-cbind(semwc,comwc,totalwc)
total
totalwc<-((comwc/totalwc)*100)
totalwc
totalwc<-round(totalwc,2)
totalwc
write.table(comwc, file = "comwc14.txt",quote = TRUE,sep = ";")
write.table(semwc, file = "semwc14.txt",quote = TRUE,sep = ";")

#############
#wc acess 17##
#############

table(ESCOLASCAPITAIS2017$IN_BANHEIRO_PNE)
semwc17<-(table(ESCOLASCAPITAIS2017$CO_UF,ESCOLASCAPITAIS2017$IN_BANHEIRO_PNE))
semwc17<-semwc17[,1]
semwc17
comwc17<-(table(ESCOLASCAPITAIS2017$CO_UF ,ESCOLASCAPITAIS2017$IN_BANHEIRO_PNE))
comwc17<-comwc17[,2]
comwc17
totalwc17<-semwc17+comwc17
totalwc17
total17<-cbind(semwc17,comwc17,totalwc17)
total17
totalwc17<-((comwc17/totalwc17)*100)
totalwc17
totalwc17<-round(totalwc17,2)
totalwc17
write.table(comwc17, file = "comwc17.txt",quote = TRUE,sep = ";")
write.table(semwc17, file = "semwc17.txt",quote = TRUE,sep = ";")

##############
#espaços 2014##
##############

table(ESCOLASCAPITAIS2014$ID_DEPENDENCIAS_PNE)
table(ESCOLASCAPITAIS2014$FK_COD_ESTADO,ESCOLASCAPITAIS2014$ID_DEPENDENCIAS_PNE)
semesp14<-table(ESCOLASCAPITAIS2014$FK_COD_ESTADO,ESCOLASCAPITAIS2014$ID_DEPENDENCIAS_PNE)
semesp14<-semesp14[,1]
semesp14
comesp14<-(table(ESCOLASCAPITAIS2014$FK_COD_ESTADO ,ESCOLASCAPITAIS2014$ID_DEPENDENCIAS_PNE))
comesp14<-comesp14[,2]
comesp14
totalesp14<-semesp14+comesp14
totalesp14
totalesppne14<-cbind(semesp14,comesp14,totalesp14)
totalesppne14
totalesp14<-((comesp14/totalesp14)*100)
totalesp14
totalesp14<-round(totalesp14,2)
totalesp14
write.table(comesp14, file = "comesp14.txt",quote = TRUE,sep = ";")
write.table(semesp14, file = "semesp14.txt",quote = TRUE,sep = ";")

##############
#espaços 2017##
##############

table(ESCOLASCAPITAIS2017$IN_DEPENDENCIAS_PNE)
table(ESCOLASCAPITAIS2017$CO_UF,ESCOLASCAPITAIS2017$IN_DEPENDENCIAS_PNE)
semesp17<-table(ESCOLASCAPITAIS2017$CO_UF,ESCOLASCAPITAIS2017$IN_DEPENDENCIAS_PNE)
semesp17<-semesp17[,1]
semesp17
comesp17<-(table(ESCOLASCAPITAIS2017$CO_UF,ESCOLASCAPITAIS2017$IN_DEPENDENCIAS_PNE))
comesp17<-comesp17[,2]
comesp17
totalesp17<-semesp17+comesp17
totalesp17
totalesppne17<-cbind(semesp17,comesp17,totalesp17)
totalesppne17
totalesp17<-((comesp17/totalesp17)*100)
totalesp17
totalesp17<-round(totalesp17,2)
totalesp17
write.table(comesp17, file = "comesp17.txt",quote = TRUE,sep = ";")
write.table(semesp17, file = "semesp17.txt",quote = TRUE,sep = ";")

#######################
#Acessibilidade: wc e vias #
#######################

###########################################
# Acesso (wcedep)-GRAFICO FINAL-EVOLUÇÃO###
###########################################

library(dplyr)
ESCOLASACESSO14<-ESCOLASCAPITAIS2014%>%filter(ESCOLASCAPITAIS2014$ID_SANITARIO_PNE==1 & ESCOLASCAPITAIS2014$ID_DEPENDENCIAS_PNE==1)
table(ESCOLASACESSO14$ANO_CENSO)
ESCOLASACESSO17<-ESCOLASCAPITAIS2017%>%filter(ESCOLASCAPITAIS2017$IN_BANHEIRO_PNE==1 & ESCOLASCAPITAIS2017$IN_DEPENDENCIAS_PNE==1)
table(ESCOLASACESSO17$NU_ANO_CENSO)

#acessibilidade total do acess2o das capit(wc+vias)/pelo total de escolas-2014

table(ESCOLASACESSO14$FK_COD_ESTADO)
ACESSO14<-table(ESCOLASACESSO14$FK_COD_ESTADO)
a<-table(ESCOLASCAPITAIS2014$FK_COD_ESTADO)
ACESSO14<-(ACESSO14/a)*100
ACESSO14<-round(ACESSO14,2)
ACESSO14
write.table(ACESSO14, file = "ac14.txt",quote = TRUE,sep = ";")

###############################################

table(ESCOLASACESSO17$CO_UF)
ACESSO17<-table(ESCOLASACESSO17$CO_UF)
b<-table(ESCOLASCAPITAIS2017$CO_UF)
ACESSO17<-(ACESSO17/b)*100
ACESSO17<-round(ACESSO17,2)
ACESSO17
write.table(ACESSO17, file = "ac17.txt",quote = TRUE,sep = ";")

#################
#wc14.csv
#wc17.csv
#dep14.csv
#dep17..csv
#fin14.csv
#fin17.csv
#################

wc14fin<-round((comwc/totalwc)*100,digits = 2)
wc14fin
write.table(wc14fin, file = "wc14.txt",quote = TRUE,sep = ";")

wc17fin<-round((comwc17/totalwc17)*100,digits = 2)
wc17fin
write.table(wc17fin, file = "wc17.txt",quote = TRUE,sep = ";")

vias14fin<-round((comesp14/totalesp14)*100,digits = 2)
vias14fin
write.table(vias14fin, file = "vias14.txt",quote = TRUE,sep = ";")

vias17fin<-round((comesp17/totalesp17)*100,digits = 2)
vias17fin
write.table(vias17fin, file = "vias17.txt",quote = TRUE,sep = ";")


#######################
#Mapas capitais conclusão.#
#######################
library(ggplot2)
library(devtools)
library(abjData)
library(magrittr)
require(RColorBrewer)
library(maps)
library(mapdata)
library(rworldmap)
library(maptools)
library(ggmap)
library(rgdal)
#########################

dados<- read.table("wc14.csv", header=TRUE, sep=";")#############Alterar csv e nao mexer na rotina

mapaUF = readShapePoly("./mapa/BRUFE250GC_SIR.shp")
plot(mapaUF)
Capitais <- read.csv("~/mestrado/2018/ArtigoAnpedSul/Municipios_Brasileiros.csv", encoding="UTF-8")                              

#RODAR CODIGO CAPITAIS
# Transforma em uma variável categórica.
dados
dados$Score = cut(dados$Score, breaks=c(0,20,40,60,80,100),
                    labels=c('0 a 20','20-40', '40-60','60-80','80-100'))
dados
paletaDeCores = brewer.pal(9, 'Greens')#Greens#OrRd#Blues
paletaDeCores = paletaDeCores[-c(2,4,6,8)]
coresDasCategorias = data.frame(Score=levels(dados$Score), Cores=paletaDeCores)
dados = merge(dados, coresDasCategorias)
dados
############################
mapaData = attr(mapaUF, 'data')
mapaData$Index = row.names(mapaData)
mapaData
names(mapaData)[3] = "UF"
mapaData = merge(mapaData, dados, by="UF")
mapaData = mapaData[order(as.numeric(mapaData$Index)),]
attr(mapaUF, 'data') = mapaData

#############################
parDefault = par(no.readonly = T)
layout(matrix(c(1,2),nrow=2),widths= c(1,1), heights=c(4,1))
par (mar=c(0,0,0,0))

# Plotando mapa

plot(mapaUF, col=as.character(mapaData$Cores))
points(capitaisIBGE$Longitude,capitaisIBGE$Latitude, pch=10,col="black",cex=1.5)
text(x = capitaisIBGE$Longitude, y = capitaisIBGE$Latitude, 
     labels = capitaisIBGE$Nome.do.Municpio, pos = 4, cex = .6)
plot(1,1,pch=NA, axes=F)
legend(x='center', legend=rev(levels(mapaData$Score)),
       box.lty=0, fill=rev(paletaDeCores),cex=.6, ncol=2,
       title='Mapa das escolas das capitais brasileiras com \n banheiros acessíveis')       



##############################
dados<- read.table("wc17.csv", header=TRUE, sep=";")
mapaUF = readShapePoly("./mapa/BRUFE250GC_SIR.shp")
plot(mapaUF)
Capitais <- read.csv("~/mestrado/2018/ArtigoAnpedSul/Municipios_Brasileiros.csv", encoding="UTF-8")                            
dados
dados$Score = cut(dados$Score, breaks=c(0,20,40,60,80,100),
                  labels=c('0 a 20','20-40', '40-60','60-80','80-100'))
dados
paletaDeCores = brewer.pal(9, 'Greens')#Greens#OrRd#Blues
paletaDeCores = paletaDeCores[-c(2,4,6,8)]
coresDasCategorias = data.frame(Score=levels(dados$Score), Cores=paletaDeCores)
dados = merge(dados, coresDasCategorias)
dados
############################################
mapaData = attr(mapaUF, 'data')
mapaData$Index = row.names(mapaData)
mapaData
names(mapaData)[3] = "UF"
mapaData = merge(mapaData, dados, by="UF")
mapaData = mapaData[order(as.numeric(mapaData$Index)),]
attr(mapaUF, 'data') = mapaData
############################################
parDefault = par(no.readonly = T)
layout(matrix(c(1,2),nrow=2),widths= c(1,1), heights=c(4,1))
par (mar=c(0,0,0,0))
plot(mapaUF, col=as.character(mapaData$Cores))
points(capitaisIBGE$Longitude,capitaisIBGE$Latitude, pch=10,col="black",cex=1.5)
text(x = capitaisIBGE$Longitude, y = capitaisIBGE$Latitude, 
     labels = capitaisIBGE$Nome.do.Municpio, pos = 4, cex = .6)
plot(1,1,pch=NA, axes=F)
legend(x='center', legend=rev(levels(mapaData$Score)),
       box.lty=0, fill=rev(paletaDeCores),cex=.6, ncol=2,
       title='Mapa das escolas das capitais brasileiras com \n banheiros acessíveis')       

############################################
dados<- read.table("vias14.csv", header=TRUE, sep=";")
mapaUF = readShapePoly("./mapa/BRUFE250GC_SIR.shp")
plot(mapaUF)
Capitais <- read.csv("~/mestrado/2018/ArtigoAnpedSul/Municipios_Brasileiros.csv", encoding="UTF-8")                              
dados
dados$Score = cut(dados$Score, breaks=c(0,20,40,60,80,100),
                  labels=c('0 a 20','20-40', '40-60','60-80','80-100'))
dados
paletaDeCores = brewer.pal(9, 'Blues')#Greens#OrRd#Blues
paletaDeCores = paletaDeCores[-c(2,4,6,8)]
coresDasCategorias = data.frame(Score=levels(dados$Score), Cores=paletaDeCores)
dados = merge(dados, coresDasCategorias)
dados
############################################
mapaData = attr(mapaUF, 'data')
mapaData$Index = row.names(mapaData)
mapaData
names(mapaData)[3] = "UF"
mapaData = merge(mapaData, dados, by="UF")
mapaData = mapaData[order(as.numeric(mapaData$Index)),]
attr(mapaUF, 'data') = mapaData
############################################
parDefault = par(no.readonly = T)
layout(matrix(c(1,2),nrow=2),widths= c(1,1), heights=c(4,1))
par (mar=c(0,0,0,0))
plot(mapaUF, col=as.character(mapaData$Cores))
points(capitaisIBGE$Longitude,capitaisIBGE$Latitude, pch=10,col="black",cex=1.5)
text(x = capitaisIBGE$Longitude, y = capitaisIBGE$Latitude, 
     labels = capitaisIBGE$Nome.do.Municpio, pos = 4, cex = .6)
plot(1,1,pch=NA, axes=F)
legend(x='center', legend=rev(levels(mapaData$Score)),
       box.lty=0, fill=rev(paletaDeCores),cex=.6, ncol=2,
       title='Mapa das escolas das capitais brasileiras com \n dependências e vias acessíveis')       

########################################

dados<- read.table("vias17.csv", header=TRUE, sep=";")
mapaUF = readShapePoly("./mapa/BRUFE250GC_SIR.shp")
plot(mapaUF)
Capitais <- read.csv("~/mestrado/2018/ArtigoAnpedSul/Municipios_Brasileiros.csv", encoding="UTF-8")                              
dados
dados$Score = cut(dados$Score, breaks=c(0,20,40,60,80,100),
                  labels=c('0 a 20','20-40', '40-60','60-80','80-100'))
dados
paletaDeCores = brewer.pal(9, 'Blues')#Greens#OrRd#Blues
paletaDeCores = paletaDeCores[-c(2,4,6,8)]
coresDasCategorias = data.frame(Score=levels(dados$Score), Cores=paletaDeCores)
dados = merge(dados, coresDasCategorias)
dados
mapaData = attr(mapaUF, 'data')
mapaData$Index = row.names(mapaData)
mapaData
names(mapaData)[3] = "UF"
mapaData = merge(mapaData, dados, by="UF")
mapaData = mapaData[order(as.numeric(mapaData$Index)),]
attr(mapaUF, 'data') = mapaData
parDefault = par(no.readonly = T)
layout(matrix(c(1,2),nrow=2),widths= c(1,1), heights=c(4,1))
par (mar=c(0,0,0,0))
# Plotando mapa
plot(mapaUF, col=as.character(mapaData$Cores))
points(capitaisIBGE$Longitude,capitaisIBGE$Latitude, pch=10,col="black",cex=1.5)
text(x = capitaisIBGE$Longitude, y = capitaisIBGE$Latitude, 
     labels = capitaisIBGE$Nome.do.Municpio, pos = 4, cex = .6)
plot(1,1,pch=NA, axes=F)
legend(x='center', legend=rev(levels(mapaData$Score)),
       box.lty=0, fill=rev(paletaDeCores),cex=.6, ncol=2,
       title='Mapa das escolas das capitais brasileiras com \n dependências e vias acessíveis')       

########################
#ACESSBILIDADE TOTAL##
########################

dados<- read.table("acess14.csv", header=TRUE, sep=";")
mapaUF = readShapePoly("./mapa/BRUFE250GC_SIR.shp")
plot(mapaUF)
Capitais <- read.csv("~/mestrado/2018/ArtigoAnpedSul/Municipios_Brasileiros.csv", encoding="UTF-8")                              
dados
dados$Score = cut(dados$Score, breaks=c(0,20,40,60,80,100),
                  labels=c('0 a 20','20-40', '40-60','60-80','80-100'))
dados
paletaDeCores = brewer.pal(9, 'OrRd')#Greens#OrRd#Blues
paletaDeCores = paletaDeCores[-c(2,4,6,8)]
coresDasCategorias = data.frame(Score=levels(dados$Score), Cores=paletaDeCores)
dados = merge(dados, coresDasCategorias)
dados
mapaData = attr(mapaUF, 'data')
mapaData$Index = row.names(mapaData)
mapaData
names(mapaData)[3] = "UF"
mapaData = merge(mapaData, dados, by="UF")
mapaData = mapaData[order(as.numeric(mapaData$Index)),]
attr(mapaUF, 'data') = mapaData
parDefault = par(no.readonly = T)
layout(matrix(c(1,2),nrow=2),widths= c(1,1), heights=c(4,1))
par (mar=c(0,0,0,0))

# Plotando mapa

plot(mapaUF, col=as.character(mapaData$Cores))
points(capitaisIBGE$Longitude,capitaisIBGE$Latitude, pch=10,col="black",cex=1.5)
text(x = capitaisIBGE$Longitude, y = capitaisIBGE$Latitude, 
     labels = capitaisIBGE$Nome.do.Municpio, pos = 4, cex = .6)
plot(1,1,pch=NA, axes=F)
legend(x='center', legend=rev(levels(mapaData$Score)),
       box.lty=0, fill=rev(paletaDeCores),cex=.6, ncol=2,
       title='Mapa das escolas das capitais brasileiras com \n acessibilidade: banheiros, dependências e vias acessíveis')       

###############################################

dados<- read.table("acess17.csv", header=TRUE, sep=";")
mapaUF = readShapePoly("./mapa/BRUFE250GC_SIR.shp")
plot(mapaUF)
Capitais <- read.csv("~/mestrado/2018/ArtigoAnpedSul/Municipios_Brasileiros.csv", encoding="UTF-8")                              
dados
dados$Score = cut(dados$Score, breaks=c(0,20,40,60,80,100),
                  labels=c('0 a 20','20-40', '40-60','60-80','80-100'))
dados
paletaDeCores = brewer.pal(9, 'OrRd')#Greens#OrRd#Blues
paletaDeCores = paletaDeCores[-c(2,4,6,8)]
coresDasCategorias = data.frame(Score=levels(dados$Score), Cores=paletaDeCores)
dados = merge(dados, coresDasCategorias)
dados
mapaData = attr(mapaUF, 'data')
mapaData$Index = row.names(mapaData)
mapaData
names(mapaData)[3] = "UF"
mapaData = merge(mapaData, dados, by="UF")
mapaData = mapaData[order(as.numeric(mapaData$Index)),]
attr(mapaUF, 'data') = mapaData
parDefault = par(no.readonly = T)
layout(matrix(c(1,2),nrow=2),widths= c(1,1), heights=c(4,1))
par (mar=c(0,0,0,0))
# Plotando mapa
plot(mapaUF, col=as.character(mapaData$Cores))
points(capitaisIBGE$Longitude,capitaisIBGE$Latitude, pch=10,col="black",cex=1.5)
text(x = capitaisIBGE$Longitude, y = capitaisIBGE$Latitude, 
     labels = capitaisIBGE$Nome.do.Municpio, pos = 4, cex = .6)
plot(1,1,pch=NA, axes=F)
legend(x='center', legend=rev(levels(mapaData$Score)),
       box.lty=0, fill=rev(paletaDeCores),cex=.6, ncol=2,
       title='Mapa das escolas das capitais brasileiras com \n acessibilidade: banheiros, dependências e vias acessíveis')      
#############
#Grafico Final##
#############

par(mfrow = c(1, 1))
plot(c("2014","2017"),c(4070,4882),  xlim=c(2014,2017), ylim=c(3500,5000), type="n",
     axes=T)
points(c("2014","2017"),c(4070,4882),lty=3, pch=19, col=10,type="o",lwd=2)
legend("top", "4053 escolas em 2014 > 4859 escolas em 2017\n 31,27% > 36,44%\n Em média: 1,72%/ano", 
       title = "Evolução da Acessibilidade entre 2014 e 2017", cex = .7, bty = "n")

#################################################
#FINAL DO SCRIPT                                                             ##
#################################################
