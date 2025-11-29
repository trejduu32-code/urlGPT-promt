Create a URL shortener app called **URLGPT by ExploitZ3r0** with the following specifications:

**Tech Stack:**

- Next.js 16 (App Router)
- TypeScript
- Tailwind CSS v4
- Upstash Redis for persistent URL storage
- shadcn/ui components


**Features:**

1. URL shortening form that generates random 6-character alphanumeric codes
2. List of shortened URLs with copy-to-clipboard and delete functionality
3. Real redirect routes at `/s/[code]` that redirect to original URLs
4. Maximum limit of 11 shortened links per user (stored in localStorage)
5. Dark theme with green accent color


**Design:**

- Dark background (`#0a0a0a`)
- Green primary/accent color for buttons and interactive elements
- Clean, minimal, professional UI
- Centered card layout with subtle border
- "by ExploitZ3r0" subtitle under the main title


**Backend:**

- API route `POST /api/shorten` to create shortened URLs (stores in Redis with `url:` prefix)
- API route `GET /api/shorten` to list all URLs
- API route `DELETE /api/shorten` to delete a URL
- Redirect route `GET /s/[code]` that looks up the code in Redis and redirects to original URL


**Deployment Configs:**
Include deployment configuration files for:

- Vercel (vercel.json)
- Render (render.yaml)
- Cloudflare Workers (wrangler.toml)
- Fly.io (fly.toml)
- Railway (railway.json)
- Docker (Dockerfile + docker-compose.yml)


**README:**
Add comprehensive README.md with step-by-step deployment instructions for Vercel, Render, Cloudflare Pages, Fly.io, Railway, Docker, DigitalOcean App Platform, and AWS Amplify. Include both GUI and CLI instructions, environment variable reference, local development setup, troubleshooting tips, and tech stack info.

**Environment Variables Required:**

- `KV_REST_API_URL` - Upstash Redis REST URL
- `KV_REST_API_TOKEN` - Upstash Redis REST token
