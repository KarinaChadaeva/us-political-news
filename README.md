## Introduction
The research is dedicated to identifying differences between the political discourse of Republicans and Democrats in the United States, based on the material from news outlets: Breitbart (Republican) and Mother Jones, Common Dreams (Democratic) for the period from May 1 to June 19, 2025.
The size of the Republican news corpus: 471,359 words; Democratic – 713,822 words.

The corpus was collected using the libraries requests and BeautifulSoup. The research employed methods such as skipgrams, sentiment analysis, and topic modeling.

## Skipgrams

### Target 'america'
__All collocates:__
<p align="center">
  <img src="plots/1.png" alt="Collocates" width="45%"/>
  <img src="plots/2.png" alt="Collocates" width="45%"/>
</p>

__1. Nouns and proper names:__
In Republican texts, words collocating with _america_ are mostly _trump, president, states, gun, war, country, israel,_ reflecting a focus on foreign policy and national security. In Democratic texts, by contrast, collocates with _america_ include _programs, deportation, expression, border, movement, detainment_ — indicating a focus on social issues and domestic policy.
<p align="center">
  <img src="plots/3.png" alt="Collocates" width="45%"/>
  <img src="plots/4.png" alt="Collocates" width="45%"/>
</p>

__2. Adjectives:__
Both groups use a similar set of descriptive words: _good, bad, great, true, critical, secure, poor, dead, domestic, conservative._
<p align="center">
  <img src="plots/5.png" alt="Collocates" width="45%"/>
  <img src="plots/6.png" alt="Collocates" width="45%"/>
</p>


### Target 'democracy'
__All collocates:__
The charts show the most frequent words appearing near _democracy_ in Republican and Democratic texts. The networks are generally similar: in both cases, connections with _freedom, people, rule, american, defend, undermine, american_ and other political terms are observed.
<p align="center">
  <img src="plots/14.png" alt="Collocates" width="45%"/>
  <img src="plots/13.png" alt="Collocates" width="45%"/>
</p>


__1. Nouns and proper names:__
The graphs are almost identical in structure, node content, and frequency characteristics, which indicates a similar conceptual context of the word _democracy_ for both sides.
<p align="center">
  <img src="plots/16.png" alt="Collocates" width="45%"/>
  <img src="plots/15.png" alt="Collocates" width="45%"/>
</p>

__2. Adjectives:__
Both parties use similar adjectives — _political, free, military, undemocratic, peaceful, authoritarian, unpatriotic, willing, principle_ — which indicates a stable context in which the concept of democracy is considered by both parties.
<p align="center">
  <img src="plots/17.png" alt="Collocates" width="45%"/>
  <img src="plots/18.png" alt="Collocates" width="45%"/>
</p>

__3. Verbs:__
The sets of verbs are also nearly the same. Both groups combine _democracy_ with verbs like _defend, get, say, destroy, believe, warn, make, stand, promote, unite, save, resist,_ and others.
<p align="center">
  <img src="plots/19.png" alt="Collocates" width="45%"/>
  <img src="plots/20.png" alt="Collocates" width="45%"/>
</p>


### Target 'migrant'
__All collocates:__
<p align="center">
  <img src="plots/22.png" alt="Collocates" width="45%"/>
  <img src="plots/21.png" alt="Collocates" width="45%"/>
</p>

__1. Nouns and proper names:__
The graph analysis shows a high level of overlap in key nouns: in both corpora, words like _child, country, deportation, government, administration, flight, refugee,_ and _detention_ stand out.

<p align="center">
  <img src="plots/23.png" alt="Collocates" width="45%"/>
  <img src="plots/24.png" alt="Collocates" width="45%"/>
</p>

__2. Adjectives:__
For both groups, words with legal and administrative context are typical, such as _illegal, legal, deportation, border, states, asylum, release_. 
<p align="center">
  <img src="plots/26.png" alt="Collocates" width="45%"/>
  <img src="plots/25.png" alt="Collocates" width="45%"/>
</p>

__3. Verbs:__
Both groups use verbs related to migration: _release, say, come, cross, include, get, make, pay, end, use, encounter,_ and others.
<p align="center">
  <img src="plots/28.png" alt="Collocates" width="45%"/>
  <img src="plots/27.png" alt="Collocates" width="45%"/>
</p>


__Conclusion:__

The results of the analysis show that the lexical context of the key words _america, democracy,_ and _migrant_ is largely similar in Republican and Democratic news sources. This may be due to the current political agenda, which is covered by both Democratic and Republican outlets. However, differences in emphasis — for example, a focus on foreign or domestic policy — point to certain ideological features of the parties.


## Nearest Neighbors 
Comparison of the 10 nearest neighbors for selected key words in the Republican and Democratic Word2Vec models reveals noticeable ideological differences in usage contexts. The word _freedom_ in the Democratic model is associated with _holiday_, _jurisdiction_, _presence_, while in the conservative model — with _terrorism_, _opposition_, _determine_. Around the word _government_, liberals show _efficiency_, _oligarchy_, _truth_, whereas Republicans lean toward more pragmatic terms like _power_, _keep_, _put_.  

Regarding _immigration_, both sides mention law enforcement agencies (_customs_, _enforcement_, _ICE_), but liberals focus more on humanitarian aspects (_bed_, _provider_), while Republicans emphasize punitive actions (_arrest_, _raid_). The topics of _climate_ and _abortion_ also demonstrate characteristic differences: the liberal model links _climate_ with _disaster_, _impact_, _environmental_, while the conservative model connects it to _strategy_, _corrupt_.  

In the case of _abortion_, the liberal model is dominated by medical and human rights contexts (_trimester_, _pill_, _safe_), while the Republican model includes more socio-educational terms (_gender_, _school_, _liberty_). These differences confirm that even in distributed vector space, political polarization is clearly reflected in lexical associations.

| word        | top-10 democrats                                                                                         | top-10 republicans                                                                                      |
|-------------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| freedom     | holiday, warning, jurisdiction, disturbing, presence, noncitizen, destination, whose, regard, pull | exactly, fully, hide, terrorism, die, example, determine, opposition, previous, nothing         |
| government  | efficiency, overthrow, oligarchy, presidency, function, loot, truth, board, sycamore, pocket       | case, put, work, power, clear, back, keep, around, seek, number                                 |
| immigration | enforcement, jersey, customs, lockup, crackdown, bed, provider, transfer, prisoner, admit          | customs, agent, federal, arrest, officer, law, assault, enforcement, raid, ice                  |
| security    | undermine, beyond, denounce, retirement, preserve, expansion, reference, modest, outlook, homeland | administration, area, homeland, states, involve, attempt, charge, stop, county, block           |
| tax         | cuts, jobs, ricks, trillion, saving, satellite, payroll, deprive, cap, adjust                      | vote, deficit, price, spending, trillion, pass, inflation, billion, tariff, might               |
| climate     | disaster, environmental, impact, structure, ownership, objection, subsidy, pretext, breed, study   | corrupt, strategic, initiative, distribute, whole, particularly, oak, strategy, mineral, detail |
| abortion    | trimester, volunteer, charge, result, course, record, field, handcuff, pill, safe                  | recent, clinic, gender, next, likely, school, education, less, index, liberty                   |
| border      | agent, fit, interrogate, writing, pen, org, visitor, relea, alistair, screen                       | carry, deportation, operation, deport, serve, operations, patrol, migrant, fine, allegedly      |
| crime       | prisoner, admit, son, lockup, monster, sad, piece, commit, parade, abortion                        | murder, court, rapist, boat, prevent, identity, expand, previous, gang, rape                    |
| election    | win, memorial, holocaust, language, dehumanizing, anguish, quite, mean, next, frustration          | quiz, primary, next, ceo, prageru, additional, vaccine, censorship, band, memorial              |



# TSNE and K-Means Clustering  
Clustering of the Republican corpus revealed several dense and interpretable semantic zones.  
![Republican clustering](plots/7.png)

In this part of the graph, we can see a clearly formed cluster dedicated to the topic of immigration, law enforcement, and power control. In the center — vocabulary connected with deportation, illegal migration, and the immigration agency ICE: _deportation_, _immigrant_, _border_, _ice_, _deport_, _arrest_, _agent_, _enforcement_, _illegal_, _alien_. This directly refers to the discourse of Donald Trump and Republican rhetoric, which focus on tightening migration policy and strengthening the southern border. Nearby are words related to protests and forceful intervention: _protester_, _riot_, _violent_, _police_, _raid_, _troop_, _national_, _guard_, _order_, _mayor_, _building_, _street_.  
![Republican clustering](plots/8.png)

In this part of the graph are lexemes connected with military topics: _gun_, _drone_, _military_, _weapon_, _missile_, _terrorist_, _war_, _defense_. Even though the semantic closeness is obvious, these words fall into different clusters — this shows some inconsistency in distributions in the vector space.  
![Republican clustering](plots/9.png)

In case of the Democrats, clusters are less clearly formed and more blurred by topic.  
![Democratic clustering](plots/10.png)

This cluster is related to questions of borders, migration, and freedom of speech. In the center — words _border_, _agent_, _press_, _journalist_, _protest_, _student_, _arrest_, _detention_, _demonstration_ — forming a socio-political agenda connected with migrant rights, detentions, street protests. Presence of words like _journalist_, _press_, _account_, _accuse_, and _criticize_ also highlights focus on freedom of information and possible conflicts between media and power structures.  
![Democratic clustering](plots/11.png)

In the next part of the graph, we see a group of words reflecting topics related to the healthcare system, social protection, and legislative initiatives: _healthcare_, _hospital_, _medical_, _doctor_, _patient_, _staff_. Also visible are words connected with law and social structure: _senator_, _amendment_, _law_, _change_, _status_, _marital_, _politic_. Presence of words like _gender_, _decline_, _system_, _need_, _worker_, and _care_ shows concern about social justice, inequality, and needed reforms.  
![Democratic clustering](plots/12.png)

__Conclusion:__
Clustering showed that in the Republican corpus, words are grouped into clear and understandable topics. For example, there is a separate cluster about immigration and power structures (ICE, deportations, protests), and also a cluster about army and weapons. This tells that Republican rhetoric is focused on security, order, and military questions.

For the Democrats, topics are more mixed, but there are also some defined groups. One of them is connected with migration, protests, and freedom of speech, another — with medicine, social protection, and laws. This shows that Democrats more often talk about social and humanitarian issues.

So, t-SNE and K-Means confirmed the difference in topic focus and rhetorical strategies of the two political camps.

## Sentiment Analysis  
Analysis of the distribution of emotionally colored words is based on three methods:

### 1. VADER

VADER is a sentiment analysis tool that works well with informal texts. It uses a lexicon of emotionally meaningful words.  
Democrats on average speak slightly more positively (mean = +0.04), but in general the news discourse is characterized by neutral tone.  
![sentiment](plots/29.png)

### 2. TextBlob

Democrats again show a more positive tone (mean = +0.06), but the difference is less significant.  
![sentiment](plots/30.png)

### 3. RoBERTa

This model was trained on ~124M tweets from January 2018 to December 2021. We chose this model because we analyze political news, and American politics is often discussed on Twitter.  
In this neural model, both groups receive negative scores, but Democrats speak even more negatively than Republicans (−0.26 vs −0.22). This can be because RoBERTa was trained on Twitter data, where negative language is used differently, and frequent criticism of government from Democrats might be interpreted as negativity.  
![sentiment](plots/31.png)

__Conclusion:__  
Different models interpret the tone of political texts in different ways.  
VADER and TextBlob detect more positive tone in Democratic texts, while RoBERTa assigns mostly negative tone to both camps, with slightly stronger shift for Democrats.


## Topic Analysis

In this research, we intentionally did not remove named entities from the corpus, because in political discourse they play an important role. Mentions of persons, countries, organizations, and key events are often thematically important elements. Considering this, for preprocessing we limited cleaning only to standard stop words.

First, we selected the optimal number of topics based on perplexity and coherence scores.  
![lda](plots/32.png)  
![lda](plots/33.png)

We chose 18 topics — with this value the model shows the best coherence and the lowest perplexity.

The graphs show the average topic distribution in the Democratic and Republican corpora.  
![lda](plots/34.png)  
![lda](plots/35.png)

In Democratic sources, topics 08, 14, and 15 dominate, each appearing on average in more than 10% of the texts. In the Republican corpus, topics 08 and 09 stand out — each of them makes up about 20% of all texts.

### Which topics are more frequent in Republican texts, and which — in Democratic?

The graph shows a normalized comparison of topic distributions between Republican and Democratic sources. On the X axis — χ-score values (the difference of average topic probabilities between groups, normalized by joint variance).  
![lda](plots/36.png)

### Most Democratic Topics:

-__Topic 00 — "War, Senate, Cryptocurrency"__  
Key words: _bill_, _war_, _senate_, _president_, _trump_, _crypto_, _congress_, _republican_, _stablecoin_, _democrats_, _democratic_  

This topic reflects the legislative agenda and discussion of key political decisions: laws, resolutions, funding. Foreign policy aspects are important (_iran_, _war_, _israel_) as well as internal politics (_congress_, _bill_, _vote_, _president_). Mention of _crypto_, _stablecoin_ may refer to regulation of cryptocurrencies.  
![lda](plots/D_00.png)

-__Topic 04 — "Students, Borders, Protests"__  
Key words: _student_, _states_, _border_, _protest_, _detention_, _free_, _deportation_, _fear_, _united_  

This topic is about social rights, protests, migration, and education.  
Words like _student_, _protest_, _free_, _detention_, _deportation_, _border_ suggest student initiatives, including immigration policy and anti-deportation movements.  
![lda](plots/D_04.png)

-__Topic 05 — "Antisemitism, Politics, Police"__  
Key words: _mamdani_, _antisemitism_, _candidate_, _jewish_, _muslim_, _police_, _state_, _law_, _lawmaker_, _speak_  

This topic raises questions of national and religious identity, civil rights, fight against antisemitism and islamophobia. Possibly also includes the Iran-Israel conflict.  
![lda](plots/D_05.png)

-__Topic 15 — "Social Security, Benefits, Veterans"__  
Key words: _social_, _security_, _benefit_, _veteran_, _healthcare_, _fund_, _accord_, _executive_, _resolution_  

This topic highlights the importance of social policy and protection. Political context is also present: _trump_, _senate_, _law_.  
![lda](plots/D_15.png)

### Most Republican Topics:

-__Topic 01 — "News, Hamas, Gaza, Patriotism"__  
Key words: _news_, _breitbart_, _hamas_, _gaza_, _attack_, _aid_, _terrorist_, _patriot_, _military_, _soliman_, _report_, _author_, _follow_  

This topic is about military conflicts in the Middle East.  
![lda](plots/R_01.png)

-__Topic 06 — "Russia, Ukraine, Trump and Media"__  
Key words: _trump_, _say_, _make_, _news_, _russia_, _ukraine_, _attack_, _breitbart_, _medium_, _post_, _parade_, _military_, _child_  

This topic relates to the conflict between Russia and Ukraine.  
![lda](plots/R_06.png)

-__Topic 08 — "Trump, President, People, Politics"__  
Key words: _trump_, _president_, _donald_, _say_, _people_, _know_, _make_, _one_, _state_, _biden_, _house_, _administration_  

This topic focuses on personalities and leadership — especially on Donald Trump. Many general political terms appear: _president_, _state_, _people_, _know_, _say_, which may refer to rhetoric, media statements, or commentary. Names like _biden_ and _musk_ also appear.  
![lda](plots/R_08.png)

-__Topic 09 — "Immigration, ICE, Law and Order"__  
Key words: _ice_, _trump_, _law_, _enforcement_, _los angeles_, _illegal_, _arrest_, _criminal_, _immigrant_, _riot_, _federal_, _newsom_, _guard_  

This topic is clearly connected with immigration and security. The word _los angeles_ appears often — probably due to recent riots in the city.  
![lda](plots/R_09.png)

## Conclusions  
In this study, we analyzed texts from Republican and Democratic news sources. We used different methods: skipgrams, word2vec models, clustering, sentiment analysis, and topic modeling.

Main findings:
- Lexical context of key words (_america_, _democracy_, _migrant_) often overlaps between corpora, but the focus is slightly different
- Word2Vec models showed that the same words can have different associations depending on the political side of the source
- Clustering revealed that Republican texts are more clearly structured by topic (for example, immigration, army, order), while Democratic ones are more diverse and spread across social and humanitarian themes (medicine, protests, migrant rights)
- Sentiment analysis gave mixed results: VADER and TextBlob find slightly more positive tone in Democratic texts, while neural model RoBERTa — more negative tone, especially for Democrats
- Topic modeling (LDA) showed that Republican sources talk more about Trump, immigration, law enforcement, and conflicts. Democratic ones focus more on social benefits, minority rights, healthcare, and freedom of speech.