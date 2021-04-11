#  FIX parser in Excel

## The following formula was used to parse the different tags in a sample FIX message.

```
MID(MID($O2,FIND(CHAR(124)&OFFSET($A$1,0,COLUMN()-1)&"=",$O2,1)+1,LEN($O2)-FIND(CHAR(124)&OFFSET($A$1,0,COLUMN()-1)&"=",$O2,1)),LEN(OFFSET($A$1,0,COLUMN()-1))+2,FIND(CHAR(124),MID($O2,FIND(CHAR(124)&OFFSET($A$1,0,COLUMN()-1)&"=",$O2,1)+1,LEN($O2)-FIND(CHAR(124)&OFFSET($A$1,0,COLUMN()-1)&"=",$O2,1)),1)-LEN(OFFSET($A$1,0,COLUMN()-1))-2)

```

## What is FIX?
Investopedia defines FIX as:
"The Financial Information eXchange (FIX) is a vendor-neutral electronic communications protocol for the international real-time exchange of securities transaction information."
[Reference: https://www.investopedia.com/terms/f/financial-information-exchange.asp]



## License
[MIT]
