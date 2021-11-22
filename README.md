<p align="center">
  <img src="/static/android-chrome-192x192.png" width="100px"/>
</p>

<h1 align="center">Welcome to Bio-Link</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.0.1-blue.svg?cacheSeconds=2592000" />
  <a href="#" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
</p>

> 🔗 A shot landing page for add to you social networks bio. Created with SvelteKit, Tailwind CSS and daisyUI.

### ✨ [Demo](https://lfv-biolink.vercel.app/)

## Screenshots

<img src="/static/2.png" alt="Screenshot 2" height="300"/> <img src="/static/1.png" alt="Screenshot 1" height="300"/> <img src="/static/3.png" alt="Screenshot 3" height="300"/> <img src="/static/4.png" alt="Screenshot 4" height="300"/>

## Configuration

Edit the `/src/config.json` file to add your data.

```json
{
  "name": "LF Verissimo",
  "description": "Front-end developer",
  "avatarUrl": "https://avatars.githubusercontent.com/u/62751844?v=4",
  "biolinkUrl": "http://lfverissimo.com",
  "theme": "dark", //You can change the daisyUI theme.
  "links": [
    //The objects will be rendered as button.
    {
      "text": "My Portfolio",
      "url": "http://lfverissimo.com"
    },
    {
      "text": "My GitHub repositories",
      "url": "https://github.com/luizfverissimo?tab=repositories"
    }
  ],
  "social": [
    //The Objects will be rendered as icon in the footer.
    {
      "icon": "faGithub",
      "url": "https://github.com/luizfverissimo"
    },
    {
      "icon": "faLinkedin",
      "url": "https://www.linkedin.com/in/lfverissimo/"
    },
    {
      "icon": "faGooglePlay",
      "url": "https://play.google.com/store/apps/developer?id=LF+Verissimo"
    }
  ]
}
```

You can switch the themes using the daisyUI avaliable theme, see more [here](https://daisyui.com/docs/default-themes), you can edit your onw theme following the [daisyUI documentation.](https://daisyui.com/docs/add-themes)

This project uses [FontAwesome Brand Icons](https://www.npmjs.com/package/@fortawesome/free-brands-svg-icons) for the social icons.

## Install

```sh
yarn # npm install
```

## Usage

```sh
yarn dev # npm run dev
```

## Build

```sh
yarn build # npm run build
yarn preview # npm run preview
```

## Deploy

To deploy this project you will need to install the correct adapter to your host – [SvelteKit Adapters](https://kit.svelte.dev/docs#adapters). It is already configurated to deploy at Vercel.

## Author

[<img alt="Logo LF Verissimo - Front-end Developer" src="https://github.com/luizfverissimo/luizfverissimo/blob/8604eedb8ecf5eeb23f8ffae63cfdf8eba6513c3/banner.png?raw=true" />](https://lfverissimo.com)

👤 **LF Verissimo**

- Website: https://lfverissimo.com
- Github: [@luizfverissimo](https://github.com/luizfverissimo)
- LinkedIn: [@lfverissimo](https://linkedin.com/in/lfverissimo)

## Show your support

Give a ⭐️ if this project helped you!

---

_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
