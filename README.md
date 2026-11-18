# Campus Stores

Campus Stores is a Product Engineer work sample set at a fictional campus media equipment desk. Work through a club’s screening, from equipment pickup to a partial return and the next morning’s handover. Open **Candidate brief** in the app for the assignment.

## Run the app

Open `index.html` in a modern browser. The app includes its scripts, styles, and icons and can run offline.

To serve it over local HTTP, run this from the repository folder and visit `http://localhost:8000`.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Each browser stores its own sample shift locally when browser storage is available. **Restart sample shift** restores the fictional starting records.

## Source

- `index.html` contains the desk layout, candidate brief, and bundled icons.
- `app.js` contains the sample records and interactions.
- `styles.css` defines the desktop and mobile layouts.

Icon license notices are in [third-party/lucide-LICENSE.txt](third-party/lucide-LICENSE.txt).


## Submit your work

1. [Fork Campus Stores](https://github.com/virinchi-healthcare/campus-stores/fork) into your GitHub account. Complete the candidate brief and push your changes to your public fork. In your README, point reviewers to your work and explain the decision you made.
2. In your fork, open **Commits**, select the final commit you want reviewed, and copy the page URL. It should look like `https://github.com/YOUR-USERNAME/campus-stores/commit/COMMIT-SHA`.
3. [Submit your work through the Google Form](https://docs.google.com/forms/d/e/1FAIpQLScvzoh1R4WS-SkiwAVBQbMvniieJYSoOEfLMyVo5CyjOvYUgQ/viewform). Your **roll number**, **email ID**, and **final commit link from your public fork** are required. Enter your roll number and email ID in the form only.


## Candidate work sample — guided kit handover

### What the existing product handles well
The original loan register creates one slip per physical unit and prevents an unavailable or out-of-scope unit from being issued. This is valuable because a partial return can be recorded without marking the whole request complete.

### What I changed
I added a **Kit workflow** view for the Film Society's RQ-214 screening. It groups the three approved units into one guided job while retaining a separate loan slip for each physical asset. The prototype walks through the same shift:

1. Friday pickup: issue the projector, speaker and adapter to Kabir, with the adapter's promised Saturday 9 am return time visible.
2. Friday evening: return the projector and speaker while leaving the adapter outstanding.
3. Saturday morning: return the adapter and close the final outstanding unit.

The workflow actions update the same loan records used by Inventory and Loan register, so the new view is not a disconnected mock-up.

### What I would keep
I would keep the physical-unit loan register, the availability checks, and the ability to record returns individually. These are the parts that preserve an accurate stock position.

### What I would observe at a real counter
I would observe whether the next-shift worker can identify the outstanding adapter and its expected arrival without asking the previous worker or searching through several messages. A practical measure would be the time taken to answer “what is still out, who has it, and when is it due?” and the number of handover clarification questions.

### Run and try the prototype
Open `index.html`, select **Kit workflow**, and use the time control to move through Friday pickup, Friday evening, and Saturday morning. The guided actions are available at the matching stage. Use **Restart sample shift** to reset the fictional data.
