Text summarization:
- multi-document summarization: https://github.com/ayushoriginal/Multi-Document-Summarization
- unsupervised multi-document abstractive summarization: https://github.com/sosuperic/MeanSum
    - paper: https://arxiv.org/pdf/1810.05739.pdf

QA:
- facebook UnsupervisedQA
    - can only answer questions based on one input paragraph
- knowledge graph + nlp (QA): https://medium.com/@mgalkin/knowledge-graphs-nlp-emnlp-2019-part-ii-56f5b03ad9ba
- KG based biology QA: https://github.com/14H034160212/HHH-An-Online-Question-Answering-System-for-Medical-Questions
- multi-document QA: https://github.com/allenai/document-qa
- list of KGQA related papers: https://github.com/BshoterJ/awesome-kgqa


KG extraction:
- general KG extraction: https://github.com/thunlp/JointNRE
    - Paper: https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/download/16691/16013
    - only has basic functionality to reproduce the results in the paper
- list of all KG related papers: https://github.com/shaoxiongji/awesome-knowledge-graph
- 中文新冠开放知识图谱：http://www.openkg.cn/dataset?q=%E6%96%B0%E5%86%A0
- Biomedical Knowledge Integration: https://github.com/tasosnent/Biomedical-Knowledge-Integration
    - seems heavy to set up


relation extraction:
- focuses on extracting biomedical entities and relations https://github.com/kbogas/medknow
    - ** seems well written, should test
    - setup pretty heavy
- some overview notes from EMNLP 2019 https://medium.com/@mgalkin/knowledge-graphs-nlp-emnlp-2019-part-ii-56f5b03ad9ba
- SemRep https://github.com/lhncbc/SemRep
    - doesn't seem to allow external data?
- Python package for relation extraction in biomedical texts: https://github.com/jakelever/kindred
    - developed to be a tool, might be useful
    - requires training data


Citation graph
- metapath2vec: https://ericdongyx.github.io/metapath2vec/m2v.html


Other Kaggle solutions
- risk factors: 
    - https://www.kaggle.com/littlesanner/build-model-of-risk-factors-on-covid-19
        - LDA + BERT feed into an AE to produce word embeddings
        - then K-Means over hashing vectorized documents to find ones closest to the risk factors, then manual summarization
    - https://www.kaggle.com/mobassir/mining-covid-19-scientific-papers#Research-Goal
        - LDA for visualization (and for finding related paper)?
        - word embedding
        - Text summarization + QA
- literature clustering
    - https://www.kaggle.com/maksimeren/covid-19-literature-clustering#COVID-19-Literature-Clustering
        - n-grams with hash vectorizer, or tfidf, with k-means/t-sne/pca
- treatment
    - https://www.kaggle.com/tarunpaparaju/covid-19-dataset-gaining-actionable-insights
        - uses word2vec to get word embedding, and then iteratively search on closest words
        - hmm drug recommendation based on w2v results?
- finding related articles via LDA
    - https://www.kaggle.com/danielwolffram/topic-modeling-finding-related-articles
- One model for all questions
    - https://www.kaggle.com/jonathanbesomi/a-qa-model-to-answer-them-all
        - uses pre-trained QA model to find answer to everything
        - has to provide context paragraph, i.e. paper
        - results are text walls...
    - https://www.kaggle.com/davidmezzetti/cord-19-analysis-with-sentence-embeddings
        - answer everything with embeddings 
- transmission
    - https://www.kaggle.com/sixteenpython/covid-19-temperature-air-travel-transmission
        - research based on outside data (coronavirus chronological data)

Not yet achieved:
- taking into account of agreement / disagreement across papers on the same topic
- knowledge extraction, e.g. entity relations
- experimental methods and results validity
- statistical meta-analysis

Tools:
- CoreNLP
    - https://stanfordnlp.github.io/CoreNLP/
- gensim
- 
