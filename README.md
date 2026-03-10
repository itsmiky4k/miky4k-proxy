# Miky4k Proxy

A proxy service for API requests, now equipped with Vercel Web Analytics.

## Features

- Claude API proxy endpoint
- Vercel Web Analytics integration for usage tracking
- Simple, clean frontend interface
- CORS-enabled API endpoints

## Project Structure

```
miky4k-proxy/
├── api/
│   └── claude.js          # Claude API proxy endpoint
├── public/
│   └── index.html         # Frontend with Web Analytics
├── package.json
├── vercel.json           # Vercel configuration
└── README.md
```

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- A Vercel account
- Anthropic API key (for Claude endpoint)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/itsmiky4k/miky4k-proxy.git
   cd miky4k-proxy
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   Create a `.env.local` file with your API keys:
   ```
   ANTHROPIC_API_KEY=your_api_key_here
   ```

### Development

Run the development server:
```bash
npm run dev
```

The site will be available at `http://localhost:3000`.

### Deployment

Deploy to Vercel:
```bash
npm run deploy
```

Or connect your GitHub repository to Vercel for automatic deployments.

## Vercel Web Analytics

This project is configured with Vercel Web Analytics. After deployment:

1. Go to your [Vercel Dashboard](https://vercel.com/dashboard)
2. Select your project
3. Click the **Analytics** tab
4. Click **Enable** to start tracking

The analytics script is already integrated in the `public/index.html` file and will automatically track page views once enabled in your Vercel dashboard.

### What's Tracked

- Page views
- Visitor counts
- Geographic data
- Browser and device information

### Viewing Analytics Data

After deployment and enabling analytics:
1. Visit your Vercel Dashboard
2. Select your project
3. Navigate to the **Analytics** tab
4. View real-time and historical data

Note: It may take a few minutes to a few hours for data to appear after first enabling analytics.

## API Endpoints

### POST /api/claude

Proxies requests to the Anthropic Claude API.

**Headers:**
- `Content-Type: application/json`

**Request Body:**
Forward the request body as per [Anthropic API documentation](https://docs.anthropic.com/claude/reference).

**Response:**
Returns the response from the Claude API.

**CORS:**
Enabled for all origins (`*`). Modify in `api/claude.js` if you need to restrict access.

## Environment Variables

Set these in your Vercel project settings:

- `ANTHROPIC_API_KEY` - Your Anthropic API key

## License

MIT

## Support

For issues or questions, please open an issue on GitHub.
