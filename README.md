# 🎬 Netflix Content Analytics Dashboard — Power BI

An interactive two-page Power BI dashboard analyzing **8,800+ Netflix titles** to uncover trends in genre popularity, content ratings, release history, and global availability. Built using a normalized relational data model with multiple tables joined on `show_id`.

---

## 📊 Dashboard Pages

### Page 1 — Overview
A high-level summary of the entire Netflix catalog with four interactive visuals:

| Visual | Chart Type | Fields Used |
|--------|-----------|-------------|
| Shows Added by Date | Area Chart | `date_added`, `type` (Movie / TV Show) |
| Top 10 Genres | Bar Chart | `netflix_listed_in.category` |
| Shows by Rating | Column Chart | `rating`, `type` |
| Countries Available | Map | `countries_released.country` |

---

### Page 2 — Single Title View
A drill-through detail page where users select any Netflix title and instantly see:

| Card | Field |
|------|-------|
| 📅 Release Year | `release_year` |
| 🎭 Rating | `rating` |
| 📝 Description | `description` |
| 🎬 Directed By | `netflix_directors.director` |
| 👥 Cast | `netflix_cast.cast` |
| 📂 Listed In | `netflix_listed_in.category` |
| 🗺️ Countries Available | `countries_released.country` (map) |

---

## 🗄️ Data Model

The dataset was normalized into multiple relational tables joined on `show_id`:

| Table | Description |
|-------|-------------|
| `netflix_data titles` | Core table — title, type, rating, release year, date added |
| `netflix_data description` | Show descriptions |
| `netflix_data netflix_directors` | Director names per title |
| `netflix_data netflix_cast` | Cast members per title |
| `netflix_data netflix_listed_in` | Genre categories per title |
| `netflix_data countries_released` | Countries where each title is available |

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** — data modeling, DAX measures, visual design
- **Power Query** — data cleaning, normalization, and table relationships
- **Microsoft Bing Maps** — geographic availability visuals
- **Power BI Service** — published for web-accessible sharing

---

## 📁 Dataset

- **Source:** [Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- **Size:** 8,800+ titles
- **Key fields:** `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `listed_in`, `description`

---

## 💡 Key Findings

- **TV-14 and TV-MA** are the two most dominant ratings, reflecting Netflix's focus on mature audiences
- **International Movies and Dramas** lead all genres, highlighting Netflix's global content strategy
- Netflix's catalog grew rapidly between **2016 and 2019**, with movies consistently outnumbering TV shows
- Content is available across a wide range of countries, with the highest concentration in **North America and Europe**

---

## 🚀 How to Open This Project

1. Download the `NetflixProject.pbix` file above
2. Open with **Power BI Desktop** — free at [microsoft.com/power-bi](https://www.microsoft.com/en-us/power-bi)
3. On Page 1, use the visuals to explore genre, rating, and content trends
4. On Page 2, use the **Movie/TV Show slicer** to search any title and view its full details

---

## 👤 Author

**Alex Larose**  
Data Analyst | Python · SQL · Power BI · Tableau  
[LinkedIn](https://linkedin.com/in/alex-larose-577b65280) · [GitHub](https://github.com/Alex9295)
