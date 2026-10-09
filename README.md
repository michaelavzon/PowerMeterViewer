# PowerMeter viewer

One web page that shows the results of the private `PowerMeter` repo on your phone: pick
Michael or Vivi, then Races, Season, Protocol or Normal, then a ride. Plots come first (tap
one to open it full size), then the report; wide tables scroll sideways with the first
column fixed. The CSV files download from buttons.

The page holds no data. It reads `RESULTS/` from your private repo through GitHub with a
read-only token that stays on your phone.

## Setup (once, about 5 minutes)

1. **New repo for the page.** github.com → **+** → **New repository** → name
   `PowerMeter-viewer`, **Public**, **Create**. Upload `index.html` (**Add file → Upload
   files**, then **Commit**). It has to be public because GitHub Pages is only free for public
   repos; anyone could see the page, but without your token it shows nothing.
2. **Turn on Pages.** In that repo: **Settings → Pages → Build and deployment → Source:
   Deploy from a branch**, branch **main**, folder **/ (root)**, **Save**. After a minute
   the page is at `https://<your-username>.github.io/PowerMeter-viewer/`.
3. **Read-only token.** github.com → your picture → **Settings → Developer settings →
   Personal access tokens → Fine-grained tokens → Generate new token**. Name
   `PowerMeter viewer`, *Repository access*: **Only select repositories → PowerMeter**,
   *Permissions → Repository permissions → Contents: Read-only*. **Generate** and copy it.
   (Use a new token, not `WORKFLOW_TOKEN`: this one can't change anything.)
4. **On the phone.** Open the page in Safari, fill in `your-username/PowerMeter` and paste
   the token, **Save and open**. Then **Share → Add to Home Screen** to get it as an app.

New results show up after a workflow run is green: tap **↻**.

If the token expires, the page says so and opens the settings; paste a new one.
