### README.md


주제: 뉴스기사의 감성지수와 원유가격(WTI)과 관계가 있을까? 

요약: https://oilprice.com 에서 2016년부터 2019년까지 게시된 원유 관련 뉴스기사 웹크롤링. 데이터 전처리. 
Loughran and McDonald(2011) 금융분야 어휘사전 기반으로 뉴스의 감성지수를 측정. 긍정적 단어는 각 +1, 부정적 단어는 각 -1의 가중치를 줌. 
감성지수는 원유 가격의 움직임과 비슷한 패턴을 보였음.
"\n",
"\n",
"\n",




1. news_crawling.ipynb

- 뉴스 데이터 수집. 뉴스 제목, 날짜, 링크 및 본문 내용 수집. CSV파일로 저장함 


2. sent_analysis.ipynb

- 데이터 전처리 및 Tokenizing
- Loughran and McDonald(2011)의 감성어휘와 뉴스 단어를 매칭  
- 매칭 된 긍정적 및 부정적 단어를 기반으로 감성지수(Sentiment) 측정. 긍정적 단어는 각 +1, 부정적 단어는 각 -1의 가중치를 줌  
- 감성지수 = 총 감성지수 / 총 긍정 및 부정 단어개수  
           = {POS * (+1) + NEG * (-1)} / (POS + NEG) 


3. draw_graph.ipynb

- matplotlib으로 감성지수 및 원유가격 그래프 그리기 
- 감성지수는 원유 가격의 움직임과 비슷한 패턴을 보였음



********** Dataset **********

aggregated.csv -> 뉴스 링크 + 본문내용

fin_pos.txt -> LM(Loughran and McDonald) 긍정 단어 리스트 

fin_neg.txt -> LM(Loughran and McDonald) 부정 단어 리스트 

sent_wti.csv -> 측정된 감성수치 + WTI(West Texas Intermediate) 원유가격   





