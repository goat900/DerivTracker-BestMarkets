# DerivTracker – BestMarkets

**Independent Deriv Analytics and Market Intelligence Platform**

DerivTracker is a web-based market analytics platform designed to connect with Deriv.com and help users monitor markets, analyze price movements and track trading performance.

## 1. Main Features

- Deriv OAuth account connection.
- Deriv account balance display (after API integration).
- Live market monitoring.
- AI DeepScan market scanner.
- Market charts and price analysis.
- Manual trade journal.
- Trading performance dashboard.
- CSV trade-history export.
- Responsive mobile and desktop interface.
- Secure backend session management.

## 2. Platform Architecture

- Frontend: HTML, CSS and JavaScript.
- Backend: Cloudflare Pages Functions.
- Hosting: Cloudflare Pages.
- Source control: GitHub.
- Session storage: Cloudflare KV.
- Trading account provider: Deriv.com.
- Market data: Deriv API.

## 3. Website

Production URL:

`https://derivtracker-bestmarkets.pages.dev`

The actual address depends on Cloudflare subdomain availability.

## 4. Installation

### Step 1: GitHub

1. Create a GitHub repository.
2. Name it `DerivTracker-BestMarkets`.
3. Upload all project files.
4. Commit the changes to the main branch.

### Step 2: Cloudflare

1. Sign in to Cloudflare.
2. Open Workers & Pages.
3. Create a Pages project.
4. Connect your GitHub repository.
5. Select the main branch.
6. Set the build command to blank.
7. Set the build output directory to `public`.
8. Deploy the website.

### Step 3: Cloudflare KV

1. Create a KV namespace.
2. Open your Pages project settings.
3. Add a KV namespace binding.
4. Set the binding name to `SESSIONS`.
5. Connect it to your newly created namespace.
6. Save and redeploy.

### Step 4: Deriv OAuth

1. Open https://developers.deriv.com/
2. Register an OAuth application.
3. Configure the application redirect URL.

Redirect URL:

`https://derivtracker-bestmarkets.pages.dev/api/oauth/callback`

4. Save your application settings.
5. Copy your client ID.
6. Configure the client ID as a server-side environment variable.
7. Never publish private OAuth secrets or customer access tokens.

## 5. Environment Variables

| Variable | Description |
|---|---|
| DERIV_CLIENT_ID | Deriv OAuth client ID |
| REDIRECT_URI | OAuth callback address |
| SESSIONS | Cloudflare KV binding |

## 6. Deriv Account Management

DerivTracker uses Deriv authorization to connect customer accounts.

Deriv remains responsible for:

- Customer trading accounts.
- Customer funds.
- Deposits.
- Withdrawals.
- Account verification.
- Trading execution and settlement.

DerivTracker does not operate an independent customer wallet.

## 7. AI DeepScan

The DeepScan module is intended to analyze:

- Selected markets.
- Recent tick movements.
- Price direction.
- Market volatility.
- Historical observations.
- Potential market opportunities.

Scanner results are informational and do not guarantee profitable trades.

## 8. Security

- Use HTTPS.
- Never request Deriv account passwords.
- Store OAuth tokens server-side.
- Validate OAuth state.
- Use PKCE.
- Protect session cookies.
- Request only necessary authorization scopes.
- Do not expose customer credentials in frontend JavaScript.

## 9. Testing

Before production use, verify:

- Website availability.
- OAuth login and callback.
- Account authorization.
- Live account balance retrieval.
- Live market subscriptions.
- DeepScan calculations.
- Trade journal storage.
- CSV exports.
- Session expiration and logout.

## 10. Disclaimer

DerivTracker – BestMarkets is an independent third-party analytics interface and is not an official Deriv product.

Trading financial and synthetic markets involves risk. Market analysis and scanner results are not financial advice or guarantees of returns.

Users connect and manage their accounts through Deriv.com.

---

**Project:** DerivTracker – BestMarkets  
**Hosting:** Cloudflare Pages  
**Backend:** Cloudflare Pages Functions  
**Account Provider:** Deriv.com  
**Repository:** DerivTracker-BestMarkets
