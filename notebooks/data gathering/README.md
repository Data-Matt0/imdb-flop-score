# Data Gathering Notebook

This notebook (`01_data_gathering.ipynb`) collects and enriches data for the IMDb Flop Score project.

## 🧾 Purpose

- Loads a dataset of the 200 lowest-rated IMDb movies (from `worst_200_movies.csv`)
- Uses the [TMDb API](https://www.themoviedb.org/documentation/api) to fetch:
  - Budget
  - Revenue
  - Release date
  - Popularity
  - Rating and vote count

## 🚀 How to Use

1. Open the notebook in Google Colab
2. Upload your local `worst_200_movies.csv` file when prompted
3. Enter your TMDb API key
4. The notebook will:
   - Search TMDb by title and year
   - Fetch movie metadata
   - Save output to `tmdb_movie_data_by_title.csv`

## 💡 Notes

- Not all movies may have a match in TMDb — that's expected for obscure or mislabeled titles
- This notebook is step 1 in a larger analysis pipeline (see root `README.md` for more)

## 📁 Output

- `tmdb_movie_data_by_title.csv`: Clean, enriched dataset with TMDb metadata
