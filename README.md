# Radix Industries corporate website concept

A local, non-production demonstration prepared for Radix decision-makers. All project imagery is conceptual. No enquiries are transmitted or stored.

## Run locally

Requires Node.js 20+ and pnpm. Run `pnpm install`, then `pnpm dev`. Run `pnpm lint` for TypeScript checks and `pnpm build` for the production build. `pnpm preview` serves the built site.

## GitHub Pages

The Vite base is `/radix-industries-demo/` and HashRouter supports direct links and refreshes under that repository path. The included workflow builds and deploys on pushes to `main`; enable GitHub Pages with GitHub Actions as its source after creating a repository and reviewing the content. Change `base` in `vite.config.ts` if the repository name differs. No repository or deployment has been created.

The demo includes `noindex` and `robots.txt` rules, but these do not make a publicly accessible site private. Access control requires a private hosting arrangement.

The client PDFs are kept separately in `work/references-private/` in the working environment and are excluded from this deliverable. Do not commit confidential materials. The form is illustrative only and must be connected to an approved service before production use.

## Verification status

The dependency lockfile was generated and TypeScript passed. A separate esbuild bundle was tested locally under `/radix-industries-demo/`: all seven direct routes loaded, the mobile menu and simulated enquiry worked, and no horizontal overflow was measured at 320, 375, 390, 430, 768, 1024, 1440, and 1920 pixels. The skip link was tested with keyboard activation.

The standard Vite production build could not be verified in the authoring environment: Windows returned `spawn EPERM` when Node attempted to start esbuild with pipes. The standalone test bundle is not the Vite output. Run `pnpm install --frozen-lockfile`, `pnpm lint`, and `pnpm build` on the intended build machine or GitHub Actions and confirm the deployment before treating this as deployment-ready. The workflow has not been run on GitHub.
