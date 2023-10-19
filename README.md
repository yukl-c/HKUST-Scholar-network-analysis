# HKUST-Scholar-network-analysis
HKUST Scholar in Department of Computer Science network analysis with Request and Beautiful Soup

Data Preparation
1. Locate the data: Faculty Profile → Scholar Profile → Publications
2. Locate the names: match name in scholar list(all english)
3. Filter out UST scholar
4. Create [coauthor, scholar] pair
5. Count numbers of each pair → Check for identical pairs → Filter out UST scholar with less than 5 collaboration(13415 → 1015 nodes)  → Append unique pair to final list

Difficulties in Data Preparation
- Inconsistency in position of scholars’ full name in link since profile does not provide full name
- Name variations (e.g. Chan, Tai Man; Chan T. M.; Chan Taiman; Chan, Alex Tai Man……)
- Spelling mistakes -> Unable to capture variations of external scholars’ name: lack of data These lead to generate more edges than actual(small portion).

Network Analysis and Validation
- use of Greedy modularity maximization
- Not fully connected (reduced edges)
- Sparse and simple communities are connected by UST scholars in big communities mainly
- Scholars outside UST seldom collaborate with other UST scholars
- li bo: common scholars between zhang qian and wang wei respectively by neighborhood measurement(common scholars between the scholars)
- Özsu, m. tamer: similar with other most by Jaccard coefficient(similarity between two scholars based on their research interests or publications)
- zhu, wenwu: strong connection with other 3 scholars by graph distance(strength of relationships between academics)

Network Construction
- Degree Centrality
  * Improtant nodes: (degree centrality > 0.05): Zhang Qian, Zhou Xiao Fang, Cheng Tim, Li Bo, Chen Lei, Yang Qiang, Guo Yike
  * highest number of neighbors and collaboration
- Betweenness Centrality
  * Improtant nodes: (degree centrality > 0.05): Zhou Xiao Fang, Yang Qiang, Chen Lei, Qu Hua Min, ni, lionel ming-shuan, zhang qian, li bo, yi ke, cheung shing
  * Bridge between those scholars who have never cooperated with each other
 
Conclusion
- Network: Sparse, made up of simple communities connected mostly by a single scholar
- Social Network Analysis:
  * Data collection: quality data → capture the reality well
  * Data processing: large amount of data → slow → reduce the dataset




