## **Pirate's Dilemma**

Captain Jack Sparrow, a brave soul on the lookout for treasures, has recently laid his hands on the latest cinematic marvel from the vast expanse of [archive.org](http://archive.org/). A true gem it be, a movie that promises laughter, tears, and the thrill of the high seas. Yet, in a twist of fate, our dear captain finds himself adrift without the crucial companion every movie marauder longs for – subtitles!

The quest is clear – to **scrape** the vast subtitle shores and uncover the hidden text that shall accompany their voyage.


## **Goal**

Create a [CLI](https://en.wikipedia.org/wiki/Command-line_interface) app using Python that accepts an mp4 file and returns a list of subtitles for it, allowing the user to choose and download their preferred option.


## **Instructions**



### Requirements

1. **Set Up Environment**
   - Create a Python virtual environment (`venv`) in the project folder.
   - Install the required modules inside the virtual environment.

2. **CLI Interface with Click**
   - Use the [click](https://click.palletsprojects.com/en/8.1.x/) module for the CLI interface.
   - The app should accept the following parameters:
     - `-l, --language`: Filter subtitles by language.
     - `-o, --output`: Specify the output folder for the subtitles.
     - `-s, --file-size`: Filter subtitles by movie file size.
     - `-h, --match-by-hash`: Match subtitles by [movie hash](https://trac.opensubtitles.org/projects/opensubtitles/wiki/HashSourceCodes).
     - `-b, --batch-download`: Enable batch mode (read further down for details).

3. **Find IMDb ID and Hash/Filesize**
   - Find the IMDb ID of the given filename
   - Depending on the options specified find the hash and filesize as well

5. **Scrape Subtitles**
   - Use `beautifulsoup4` to scrape [opensubtitles](https://www.opensubtitles.org/en/search/subs) and get the list of subtitles.
   - Follow these guidelines:
     - Search using the IMDb ID and movie hash/file size (bonus points if you can come up with an algorithm to search using a selection of the three to maximise the chances of getting a result)
     - Apply the specified filters.
     - Sort the results by "Downloaded" in descending order.

6. **Download Subtitles**
   - List all the subtitles available for the given movie
   - Prompt the user to choose one and download it.

7. **Batch Mode**
   - If batch mode is enabled, a directory should be specified instead of a single file.
   - Automatically download subtitles for all movies within the specified directory instead of listing and prompting.

8. **User Interface**
   - Provide a clean user interface with loading indicators and basic error handling.

9. **Validation**
   - Test the app to ensure it works by using this [movie file](https://archive.org/download/plan-9-from-outer-space/plan-9-from-outer-space.mpeg4).


## **Resources**



* [Open Subtitles](https://www.opensubtitles.org/en/search)
* [Click Documentation](https://click.palletsprojects.com/en/8.1.x/)
* [BS4 Documentation](https://www.crummy.com/software/BeautifulSoup/)

This is by no means an exhaustive list of references; don't be scared to Google and locate the rest yourself! After all, for a developer, googling is a very important skill to learn :)

