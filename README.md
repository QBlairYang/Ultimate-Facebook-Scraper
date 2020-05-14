### Start
```bash
$ git clone https://source.developers.google.com/p/mfe2020-risk-team-r1/r/github_qblairyang_ultimate-facebook-scraper
$ cd Ultimate-Facebook-Scraper

# Set up a virtual env
$ python3 -m venv venv
$ source venv/bin/activate
```

### How to Run

- Fill your Facebook credentials into [`credentials.yaml`](credentials.yaml)
- Edit the [`input.txt`](input.txt) file and add profile, groups and individual group posts links as you want in the following format with each link on a new line:

Make sure the link only contains the username or id number at the end and not any other stuff. Make sure its in the format mentioned above.

```python
$ python scraper/scraper.py
```

> Note: There are two modes to download Friends Profile Pics and the user's Photos: Large Size and Small Size. By default they are set to Small Sized Pics because its really quick while Large Size Mode takes time depending on the number of pictures to download.

You can personalize your scrapping needs using the command line arguments:

```python
$ python scraper/scraper.py \
    --uploaded_photos True \
    --friends_photos True \
    --friends_small_size True \
    --photos_small_size True \
    --total_scrolls 2500 \
    --scroll_time 8
```

