# Tech Conference 2025

This project is a Svelte-based web application for the Tech Conference 2025. It includes various features such as a countdown timer, speaker information, schedule, venue details, and more.

## Project Setup

To set up the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Tech-Conference.git
   cd tech-conference-2025
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

   You can also start the server and open the app in a new browser tab:
   ```bash
   npm run dev -- --open
   ```

## Building for Production

To create a production version of your app:
```bash
npm run build
```

You can preview the production build with:
```bash
npm run preview
```

> To deploy your app, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.

## Features

- **Countdown Timer**: A countdown timer that shows the time left until the event starts. The timer updates every second.
- **Speaker Information**: A section that displays information about the speakers, including their names, titles, bios, and photos.
- **Schedule**: A detailed schedule of the event, including the date, time, topic, and speaker for each session.
- **Venue Details**: Information about the venue, including an embedded Google Maps location, accessibility options, amenities, and instructions for attendees.
- **Dark Mode**: A dark mode toggle that allows users to switch between light and dark themes.
- **Responsive Design**: The application is fully responsive and works well on both desktop and mobile devices.
- **Social Media Links**: Links to the conference's social media pages, including Twitter, Facebook, LinkedIn, and Instagram.

## Contributing

If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Make your changes and commit them with a clear message.
4. Push your changes to your fork.
5. Create a pull request to the main repository.
