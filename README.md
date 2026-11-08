# MopTube

A video site you can run as a desktop app. Channels, long videos, Mops (short vertical videos), comments, likes and a creator studio, all in one window.

MopTube is an independent project and is not affiliated with YouTube or Google.

## Status, honestly

- This is an early version. Everything is stored on the computer it runs on, so nobody else can see your videos yet.
- There are no accounts. The app is one channel per computer.
- View, like and subscriber numbers count activity on this computer only.
- Installers are not code-signed, so Windows and macOS show a warning the first time you open the app.

## Quick start

You need [Node.js](https://nodejs.org) 20 or newer.

```
git clone https://github.com/YOUR_GITHUB_USERNAME/moptube.git
cd moptube
npm install
npm start
```

## What works

| Feature | State |
| --- | --- |
| Channel: name, username, picture, banner, description, links | Done |
| Image trimming for banner, picture and thumbnails | Done |
| Upload videos up to 15 minutes, with title, description and thumbnail | Done |
| Watch page with speed and quality settings | Done |
| Comments with replies, likes and dislikes | Done |
| Mops: vertical videos up to 3 minutes in a swipe feed | Done |
| Home page with a Mops row and recommended videos | Done |
| Search | Done |
| Creator Studio: dashboard, content, analytics, comments | Done |
| Light and dark themes | Done |
| One view per viewer for each video | Done (per computer) |
| Desktop installers for Windows, Mac and Linux | Done (built by GitHub) |
| Accounts and login | Planned |
| Online storage so people can see each other's videos | Planned |
| Real subscriptions and notifications | Planned |
| Playlists | Planned |
| Reporting and moderation tools | Planned |

The quality option on the watch page shrinks the picture in the viewer. It does not switch between separate files.

## Run it yourself

### What you need

- Node.js 20 or newer
- git, if you want to clone the repository

### Install and start

```
npm install
npm start
```

### Build an installer on your own machine

```
npm run dist
```

The installer for the system you are on appears in the `dist/` folder.

### Publish downloads on GitHub

1. Create a repository on GitHub and push this project to it.
2. In `package.json`, replace `YOUR_GITHUB_USERNAME` and `YOUR NAME`.
3. Create and push a version tag:

```
git tag v0.1.0
git push origin v0.1.0
```

The workflow in `.github/workflows/build.yml` builds the Windows (.exe), Mac (.dmg) and Linux (.AppImage) installers and attaches them to a release. People download them from the **Releases** page.

## Project layout

| Path | What it holds |
| --- | --- |
| `src/index.html` | The whole app: pages, styles and code |
| `main.js` | Opens the app window and sends web links to the normal browser |
| `build/icon.png` | The app icon |
| `package.json` | App details, scripts and installer settings |
| `.github/workflows/build.yml` | Builds the installers on GitHub |

## Next steps

To let people see each other's videos, MopTube needs accounts, a database and online video storage. Firebase (Authentication, Firestore and Storage) is the planned choice.

## License

Not chosen yet. Until a license is added, all rights are reserved. Pick one before making the repository public.
