# Privacy Policy — yt-live-status

**Effective date:** June 2026  
**Developer:** ReserveAggressive458

---

## 1. Overview

yt-live-status is a Reddit Devvit app that monitors a YouTube channel and posts stream status updates to a subreddit. This policy describes what data the app stores and how it is used.

**The app does not collect, store, or transmit any personal information about Reddit users.**

## 2. Data stored

The app stores the following data in Devvit Redis (Reddit's built-in key-value store), scoped to the subreddit where the app is installed. None of this data identifies individual users.

| Data | Purpose |
|---|---|
| YouTube channel ID | Identifies the channel being monitored |
| YouTube video ID of the active stream | Tracks the current live video |
| Reddit post IDs (live and offline threads) | Allows the app to manage and update its own posts |
| Timestamps | Used to control poll intervals and offline cooldown logic |
| YouTube API key (subreddit setting) | Authenticates requests to the YouTube Data API v3 |

All stored data is automatically cleared when the app is uninstalled.

## 3. Data not collected

This app does not collect:

- Reddit usernames, user IDs, or any user account information
- Comment or post content from subreddit members
- Voting, karma, or engagement data
- Any information about visitors to the subreddit

## 4. External services

The app makes outbound HTTPS requests to the following services:

- **www.youtube.com** — to fetch a channel's public RSS feed. No API key is sent. The only data transmitted is the channel ID.
- **youtube.googleapis.com** — to call the YouTube Data API v3 to verify live stream status. The YouTube API key configured by the moderator is sent as part of these requests.

No data received from these services is stored beyond what is listed in section 2. No data is sent to any other third party.

## 5. Data retention

All app data is stored in Devvit Redis and is scoped to the installing subreddit. Data persists as long as the app remains installed. It is cleared automatically on uninstall, or on request via the app's reset endpoint.

## 6. Children's privacy

This app is not directed at anyone under the age of 13 and does not knowingly collect data from minors. Reddit's own age restrictions apply.

## 7. Changes

This policy may be updated from time to time. The effective date at the top of this page will reflect the most recent revision.

## 8. Contact

For privacy-related questions or concerns, contact the developer via Reddit: [u/ReserveAggressive458](https://www.reddit.com/user/ReserveAggressive458).
