# 🎬 Movie Analytics Dashboard: Clustering, Recommendations & Visualisation

This project combines two key disciplines — **Machine Learning for Business** and **Data Visualisation** — to deliver a complete movie analytics solution. It focuses on clustering films by genre, generating personalized recommendations, and visualizing key user and genre insights through a fully interactive dashboard.

Built for a **young audience (18–35 years old)**, the platform enhances movie discovery by making use of clustering, collaborative filtering, content-based filtering, and engaging visual narratives powered by **Streamlit** and **Plotly**.

---

## 🧠 Machine Learning for Business Module

### 📌 Clustering Movies by Genre

- Dataset features: `title`, `genres`, `year`
- Preprocessing: 
  - Extracted release year using regex
  - Multi-label one-hot encoding of `genres`
  - Normalized features with `StandardScaler`

#### 🔍 Clustering Algorithms Tested:
| Algorithm          | Features         | Silhouette Score |
|--------------------|------------------|------------------|
| K-Means            | Genres           | **0.232**        |
| K-Means            | Genres + Year    | 0.148            |
| K-Medoids          | Genres           | 0.203            |
| Hierarchical (Ward)| Genres           | 0.128            |

- **Best Result**: K-Means with genres only.
- **Insight**: Multi-genre overlap (e.g., Comedy | Drama | Romance) limits cluster purity.
- **Recommendation**: Use K-Means with genre encoding for scalable clustering.

### 🤝 Movie Recommender Systems

#### 📊 Models Implemented:

- **User-User Collaborative Filtering**  
- **Item-Item Collaborative Filtering**  
- **Content-Based Filtering (based on genres)**

#### ✅ Results:

- **Best Performance**: User-User filtering — highly personalized, diverse suggestions.
- Content-based filtering ensured thematic accuracy but lacked novelty.
- Item-based filtering grouped popular titles but missed personalized depth.

#### 💡 Hybrid Recommendation:

- Combining collaborative + content-based filtering is ideal.
- Solves cold-start problems and improves diversity/accuracy of suggestions.

---

## 📊 Data Visualisation Module

Built for usability and clarity, the dashboard includes 5 interactive visualizations optimized for performance and aesthetics.

### 📈 Visual Components:

1. **Genre Popularity vs. Average Rating**  
   - Bubble chart showing vote count (X), genre (Y), average rating (color/size)

2. **Top 5 Movies by Genre**  
   - Horizontal bar chart with average ratings of best movies in each genre

3. **Genre Trends Over Time**  
   - Animated horizontal bar chart showing genre evolution year-by-year

4. **Top 10 Similar Movies by Genre**  
   - Genre-based similarity percentage bar chart for a selected movie

5. **User Behavior Radar Chart**  
   - Shows user profile across:
     - Avg. rating
     - Variability (std)
     - Film count
     - % of high ratings
     - Genre diversity (entropy)

### 🎯 Dashboard Design Priorities

- **Interactivity**: Filters by genre, year, user, movie
- **Clarity & Simplicity**: Vibrant but clean aesthetics, smooth animations
- **Accessibility**: Neutral language, viridis palette for color blindness
- **Performance**: Optimized for fast loading and smooth transitions

---

## 🧪 Data Preparation

- Merged movies and ratings datasets
- Cleaned missing/duplicate values and dropped irrelevant columns
- Titles cleaned (years removed) for clarity
- One-hot encoded genres for metrics and filtering
- Applied thresholds (e.g., min. 100 votes) to reduce bias
- Normalized user metrics using `MinMaxScaler`

---

## 🚀 Deployment

- 🎛️ **Interactive App**: [Streamlit Dashboard](https://appca2py-bwz9dgjguscjbipn8ijpvt.streamlit.app/)
- 💻 **GitHub Repo**: [AntonioGiambra/Movies_Analysis](https://github.com/AntonioGiambra/Movies_Analysis)

---

## 📚 References

- Akmal, A. (2024). *Less is More in User Experience Design*. [Medium](https://medium.com/@abiyouakmal/less-is-more-in-user-experience-design-the-paradox-of-choice-82adff28e940)
- ChartExpo (2025). *Radar Charts Simplified*. [chartexpo.com](https://chartexpo.com/blog/radar-chart#)
- McNamee, S. (2025). *Social Media Stats in the UK*. [Sprout Social](https://sproutsocial.com/insights/social-media-statistics-uk/)
- Raval, T. (2024). *Digital Transformation for Millennials & Gen Z*. [Forbes](https://www.forbes.com/councils/forbestechcouncil/2019/08/20/digital-transformation-in-the-age-of-millennials-and-gen-z/)
- tenscope (2024). *Data Visualization Principles for Clarity*. [Tenscope Blog](https://www.tenscope.com/post/data-visualization-design-principles-for-clarity)
- uptrends (2018). *Web Performance Psychology*. [Uptrends Blog](https://blog.uptrends.com/web-performance/the-psychology-of-web-performance/)

---

## 🧾 Summary

This project illustrates how **machine learning models** and **visual design principles** can be effectively combined to support decision-making in digital media platforms. From segmenting movies and generating recommendations to building visually engaging dashboards, this work highlights the power of cross-disciplinary data applications.

