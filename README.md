# Political Action Events · CCCTU Local 1600

A mobile-friendly page listing upcoming political action events for members of the Cook County College Teachers Union, AFT-IFT Local 1600.

Live page (once GitHub Pages is on): https://troyaswanson.github.io/LegEventLandingPage/

## How it works

- Events live in the **Political Events** Google Sheet, on the **Events** tab, one row per event.
- The Events tab is published to the web as a CSV link. The page reads that link in each visitor's browser every time it opens, so sheet changes appear within a few minutes.
- This repository holds only the page code and the union seal. It holds no event data.

## Sheet columns

Publish, Title, Type, Date, Start Time, End Time, Location Name, Address, Sign-up link, Sign-up label, Contact name, Contact email, Notes, Check

- Only rows with **Publish** checked and both **Title** and **Date** filled in appear.
- Start the title with **CANCELLED** or **POSTPONED** to show a badge.
- With no sign-up link, the event shows "To sign up, contact [name]: [email]."
- Times are Central time. Events drop off after they end.
- Everything on the Events tab is public, including the Notes column.

## Changing the sheet link

The CSV link is set near the top of the script in `index.html` (`CSV_URL`). When the sheet moves to a union account, publish the new sheet's Events tab as CSV and replace that one line.

## Testing

Add `?csv=<link>` to the page address to read a different CSV, and `?now=2026-12-01T09:00:00-06:00` to see the page as of another date.
