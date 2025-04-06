# Learn FinTech Platform

An interactive learning platform leveraging AI and YouTube content to create engaging FinTech educational experiences.

## Features

- Interactive YouTube-based course player
- AI-generated quizzes to test understanding
- Progress tracking and gamification
- Community challenges and leaderboards
- Mental wellness tracking and recommendations

## Development

To start the application:

```bash
npm run dev
```

The application will be available at http://localhost:5000

## Ngrok Tunneling

The application supports ngrok tunneling to make it accessible from the internet. This is useful for sharing the application with others or for testing on mobile devices.

### Start ngrok tunnel

Run the following command in a separate terminal:

```bash
npx tsx server/start-tunnel.ts
```

The public URL will be printed in the console. The URL looks like: `https://xxxx-xx-xxx-xxx-xxx.ngrok-free.app`

### Stop ngrok tunnel

To stop the ngrok tunnel:

```bash
npx tsx server/stop-tunnel.ts
```

## Tech Stack

- Frontend: React, TypeScript, TailwindCSS, Shadcn UI
- Backend: Express, Node.js
- Database: PostgreSQL with Drizzle ORM
- APIs: Gamini API (for quiz generation), YouTube API (for video content)
### Tunnel to External URL

You can create a tunnel to an external URL using the following command:

```bash
npx tsx server/tunnel-to-url.ts
```

This will create a tunnel to the default URL specified in the `server/tunnel-to-url.ts` file.

You can also specify a custom URL:

```bash
npx tsx server/tunnel-to-url.ts --url=your-custom-domain.com --port=8080
```

Additional options:
- `--subdomain=<name>` - Use a custom subdomain for your ngrok URL
- `--region=<region>` - Use a specific ngrok region

### Custom Tunnel Options

For more advanced tunnel configurations, you can pass options to the tunnel script:

```bash
npx tsx server/start-tunnel.ts --subdomain=myapp --region=eu
```

Available options:
- `--subdomain=<name>` - Use a custom subdomain (requires ngrok Pro)
- `--url=<url>` - Tunnel to a custom URL instead of local port
- `--region=<region>` - Use a specific ngrok region (us, eu, ap, au, sa, jp, in)

