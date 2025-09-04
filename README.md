# Email Tracking Dashboard

A web-based dashboard for tracking and analyzing email opens through pixel tracking. This application helps classify delivery fetches vs real opens by counting pixel requests per recipient.

## Features

- **Real-time Log Parsing**: Parse server logs to extract email tracking data
- **Smart Classification**: Distinguish between email delivery fetches and actual opens using configurable thresholds
- **Interactive Dashboard**: View statistics including distinct emails, confirmed opens, and open rates
- **Filtering & Sorting**: Filter by status (confirmed/pending) and sort by hit count
- **CSV Export**: Export tracking data to CSV format for further analysis
- **Dark Theme UI**: Modern, responsive interface with a professional dark theme

## Deployment to Vercel

### Prerequisites

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Create a Vercel account at [vercel.com](https://vercel.com) if you don't have one

### Deploy Using Vercel CLI

1. Navigate to the email folder:
```bash
cd email
```

2. Run the deployment command:
```bash
vercel
```

3. Follow the prompts:
   - Confirm the project setup
   - Choose a project name (or use the default)
   - Link to an existing project or create a new one

4. For production deployment:
```bash
vercel --prod
```

### Deploy Using Git Integration

1. Push this folder to a GitHub repository
2. Go to [vercel.com](https://vercel.com) and sign in
3. Click "New Project"
4. Import your GitHub repository
5. Configure the project:
   - **Root Directory**: Set to `email` if this is in a subdirectory
   - **Framework Preset**: Select "Other"
6. Click "Deploy"

### Environment Configuration

No environment variables are required for this static application.

### Custom Domain (Optional)

After deployment, you can add a custom domain:

1. Go to your project settings on Vercel
2. Navigate to the "Domains" section
3. Add your custom domain
4. Follow the DNS configuration instructions

## Local Development

To run locally with Vercel dev server:

```bash
npm install
npm run dev
```

The application will be available at `http://localhost:3000`

## Project Structure

```
email/
├── email.html          # Main application file
├── vercel.json        # Vercel configuration
├── package.json       # Project metadata and scripts
├── .vercelignore      # Files to ignore during deployment
└── README.md          # This file
```

## Configuration Details

The `vercel.json` file includes:
- **Clean URLs**: Removes .html extensions from URLs
- **Security Headers**: Adds X-Frame-Options, X-Content-Type-Options, and X-XSS-Protection
- **Caching**: Sets appropriate cache headers for performance
- **Routing**: Routes all requests to email.html

## Usage

1. **Paste Server Logs**: Copy your server logs containing email tracking pixel requests
2. **Set Threshold**: Configure how many hits constitute a "confirmed" open
3. **Parse Logs**: Click "Parse Logs" to process the data
4. **View Results**: Analyze the dashboard statistics and individual email tracking data
5. **Export Data**: Use "Export CSV" to download the results

## Support

For issues or questions about deployment, refer to the [Vercel documentation](https://vercel.com/docs).
