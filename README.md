# Drive Log

Time your drives, see where you got held up, and know what each journey costs in fuel. It runs in the browser on your phone, with no app store and no account.

**Open it:** https://stephenbeale.github.io/drive-log/ (on your phone, use *Add to Home Screen* for an app icon).

## What it does

- **One-press regular journeys.** Commute, school run, heading home and so on, each with the time it usually takes at this time of day.
- **Hands-free while you drive.** With location on, it tracks distance and speed and spots slow traffic by itself. Stop for a while and it offers a break. Stop near your destination and it offers to end the journey. A break ends by itself when you drive off.
- **Share on WhatsApp.** Send your ETA before you set off, or a summary of a finished drive with a link to the route.
- **Route map.** Records the path you drove. Sharing it (an image, a GeoJSON file or a Google Maps link) can hide the mile around the start and finish, plus postcodes and times, so the route doesn't reveal where you live or work.
- **Insights per route.** Typical, quickest and slowest times, broken down by the time you set off, the day of the week, and term time versus school and bank holidays.
- **Several cars.** Pick the car when you start a drive. Each one has its own MPG and fuel price.
- **Fuel tracking.** Photograph the receipt at each fill-up and the litres, price and total are filled in for you. Fill to the brim and note the mileage, and it works out your real MPG and cost per mile. Your latest price feeds straight into the fuel cost of each drive.
- **Photos instead of typing.** Dashboard mileage and fuel receipts can be photographed. On this site the text is read on your phone (Tesseract), so check the numbers. In the Claude-hosted version, Claude reads them.

Never use the phone while driving. Set the drive up before you go, leave the phone in its mount, and add anything you missed once you've parked.

## Where your data lives

Everything is stored in your browser on your device (`localStorage`). Nothing is sent anywhere. Use **Export CSV** on the Log tab to keep a copy.

## Files

- `drive-log.artifact.html` is the page source. It also runs as a Claude artifact, where drives sync to your Claude account and Claude names places and reads mileage photos.
- `build.sh` wraps it into `index.html` for GitHub Pages. Run it after editing the source.
