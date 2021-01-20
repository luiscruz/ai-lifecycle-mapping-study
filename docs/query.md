---
layout: default
---
# Query

## The query for DBLP

```
ai | ml | artificial | machine| neural | deep | dl 
ai | ml | artificial | machine | network | deep | dl 
ai | ml | artificial | machine| neural | learning | dl 
ai | ml | artificial | machine | network | learning | dl
ai | ml | artificial | learning| network | deep | dl 
ai | ml | artificial | learning| neural | deep | dl 
ai | ml | artificial | learning| network | learning | dl 
ai | ml | artificial | learning| neural | learning | dl 
ai | ml | intelligence | machine| neural | deep | dl 
ai | ml | intelligence | machine | network | deep | dl 
ai | ml | intelligence | machine| neural | learning | dl 
ai | ml | intelligence | machine | network | learning | dl
ai | ml | intelligence | learning| network | deep | dl 
ai | ml | intelligence | learning| neural | deep | dl 
ai | ml | intelligence | learning| network | learning | dl 
ai | ml | intelligence | learning| neural | learning | dl
traceab | reproduc| verif | guideline | standard | lifecycle| pipeline | deploy | maintain | fairness | transparency | platform
```

## The query for Scopus

```
TITLE-ABS-KEY ( "ai model*"  OR  "ml model*"  OR  "artificial intelligence model*"  OR  "machine learning model*"  OR  "neural network model*"  OR  "deep learning model*"  OR  “dl model*" ) 

AND TITLE-ABS-KEY ( traceab*  OR  reproduc*  OR  guideline  OR  standard*  OR  lifecycle  OR  deploy*  OR  verif*  OR  platform  OR  maintain*  OR  fairness )  

AND  TITLE ( "ai"  OR  "ml"  OR  "artificial intelligence"  OR  "machine learning"  OR  "neural network"  OR  "deep learning"  OR  "dl" )  

AND NOT  TITLE-ABS-KEY ( sensor )  

AND NOT  TITLE ( predict*  OR  forecast* )  

AND NOT  TITLE ( "deep learning method for"  OR  "dl method for"  OR  "ai method for"  OR  "ml method for"  OR  "artificial intelligence method for"  OR  "machine learning method for"  OR  "neural network method for" )  

AND NOT  TITLE ( "deep learning approach for"  OR  "dl approach for"  OR  "ai approach for"  OR  "ml approach for"  OR  "artificial intelligence approach for"  OR  "machine learning approach for"  OR  "neural network approach for" )  

AND NOT  TITLE ( ( "using"  PRE/2  "deep learning" )  OR  ( "using"  PRE/2  "dl" )  OR  ( "using"  PRE/2  "ai" )  OR  ( "using"  PRE/2  "ml" )  OR  ( "using"  PRE/2  "artificial intelligence" )  OR  ( "using"  PRE/2  "machine learning" )  OR  ( "using"  PRE/2  "neural network" ) )  

AND NOT  TITLE ( ( "Application of"  PRE/2  "dl" )  OR  ( "Application of"  PRE/2  "ai" )  OR  ( "Application of"  PRE/2  "ml" )  OR  ( "Application of"  PRE/2  "artificial intelligence" )  OR  ( "Application of"  PRE/2  "machine learning" )  OR  ( "Application of"  PRE/2  "neural network" ) )  

AND NOT  TITLE ( ( "Application of"  PRE/2  "deep learning" )  OR  ( "based on"  PRE/2  "dl" )  OR  ( "based on"  PRE/2  "deep learning" ) )  

AND NOT  TITLE ( ( "by"  PRE/2  "deep learning" )  OR  ( "by"  PRE/2  "dl" )  OR  ( "by"  PRE/2  "ai" )  OR  ( "by"  PRE/2  "ml" )  OR  ( "by"  PRE/2  "artificial intelligence" )  OR  ( "by"  PRE/2  "machine learning" )  OR  ( "by"  PRE/2  "neural network" ) )  

AND NOT  TITLE ( ( "based on"  PRE/2  "ai" )  OR  ( "based on"  PRE/2  "ml" )  OR  ( "based on"  PRE/2  "artificial intelligence" )  OR  ( "based on"  PRE/2  "machine learning" )  OR  ( "based on"  PRE/2  "neural network" ) )  

AND NOT  TITLE ( ( "diagno*"  OR  "defect"  OR  "fault" ) )  
AND NOT  TITLE ( fpga ) ) 
```

## Explanation

### DBLP
For DBLP "|" means Boolean "or", and space " " means Boolean "and".

The phrase search operator (.) was disabled due to technical problems, and dblp does not support brackets to indicate the order of precedence rules. For example, to express: 

"Artificial Intelligence" or AI

We had to split the phrase "Artificial Intelligence". This led to the search query: 

"Artificial| AI Intelligence | AI"

Instead of "Artificial Intelligence | AI"

The wrong query "Artificial Intelligence | AI" will only the noise papers that contain "Artificial AI" or "Intelligence AI" instead of the desired papers containing "Artificial Intelligence" or "AI".

The correct query (Artificial| AI Intelligence | AI) identifies papers that contain "Artificial Intelligence" or "AI", as well as some "noise" papers that contain "Artificial AI" or "Intelligence AI". If the wrong query is used, such as "Artificial Intelligence | AI",

Taking the above into account, we defined our DBLP search queries as shown above. To make it easy to read, we used separate lines to represent a space " ".

### Scopus

Scopus accepts the Boolean "and not"; therefore, we also defined keywords to filter out papers that were out of our research scope to reduce the workload in the next step. We named these as exclusive keywords. In this work, we only focused on AI model lifecycle management and not on the applications of AI, using AI to predict or forecast something, or using AI to detect defects, etc. The exclusive keywords are as follows: 
predict, forecast, diagnosis, defect, fault, fpga, sensor application, AI method for, using PRE/2 AI, AI approach for, "Application of" PRE/2 "AI", by PRE/2 AI, "based on" PRE/2 AI.
