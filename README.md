# Drive Log

Time your drives, see where you got held up, and know what each journey costs in fuel. It runs in the browser on your phone, with no app store and no account.

**Open it:** https://stephenbeale.github.io/drive-log/ (on your phone, use *Add to Home Screen* for an app icon).

## What it does

- **One-press regular journeys.** Commute, school run, heading home and so on, each with the time it usually takes at this time of day.
- **Hands-free while you drive.** With location on, it tracks distance and speed and spots slow traffic by itself. Stop for a while and it offers a break. Stop near your destination and it offers to end the journey. A break ends by itself when you drive off.
- **Route map.** Records the path you drove. Sharing it (an image, a GeoJSON file or a Google Maps link) can hide the mile around the start and finish, plus postcodes and times, so the route doesn't reveal where you live or work.
- **Insights per route.** Typical, quickest and slowest times, broken down by the time you set off, the day of the week, and term time versus school and bank holidays.
- **Fuel cost.** From your car's real-world MPG and the price per litre.
- **Mileage.** Type it in, or take a photo of the dashboard (reading the photo automatically only works in the Claude-hosted version).

Never use the phone while driving. Set the drive up before you go, leave the phone in its mount, and add anything you missed once you've parked.

## Where your data lives

Everything is stored in your browser on your device (`localStorage`). Nothing is sent anywhere. Use **Export CSV** on the Log tab to keep a copy.

## Files

- `drive-log.artifact.html` is the page source. It also runs as a Claude artifact, where drives sync to your Claude account and Claude names places and reads mileage photos.
- `build.sh` wraps it into `index.html` for GitHub Pages. Run it after editing the source.
