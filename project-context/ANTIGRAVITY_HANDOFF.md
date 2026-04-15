# Antigravity Handoff  ## Project Your Project Name  ## Project Slug your-project-slug  ## Task Task title  ## Task Slug task-slug  ## GitHub Issue - Number: 44 - URL: https://github.com/AshokSahani7390/Antigravity-Automation/issues/44  ## Repository https://github.com/yourname/your-repo  ## Branching - Default Branch: main - Target Branch: develop  ## Read These Files First - /project-context/MASTER_CONTEXT.md - /project-context/CURRENT_TASK.md - /project-context/TESTING_STRATEGY.md - /project-context/ANTIGRAVITY_HANDOFF.md  ## Current Goal What should be done in this task.  ## Planning Summary # Planning Summary
This implementation plan outlines the systematic approach to completing the **Task title** for the **Your Project Name** MVP. The focus is on delivering a production-grade feature that aligns with the high-end UI/UX requirements while ensuring deep integration with the established tech stack (Next.js, Supabase, Clerk). Every step follows a "test-first, build-second" methodology to maintain stability in the `develop` branch.

## Goal
The primary objective is to execute: **What should be done in this task.**  
This involves building modular components, ensuring secure backend operations, and implementing premium motion design.

## Scope
*   **Frontend:** UI implementation using Tailwind CSS, GSAP for premium motion, and Radix/Lucide for icons.
*   **Backend:** Supabase Edge Functions or Next.js Server Actions for logic.
*   **Security:** Clerk authentication checks and server-side validation.
*   **Testing:** Unit tests for business logic and E2E tests for the user flow.
*   **Analytics/Monitoring:** Integration of PostHog events and Sentry error tracking.

## Existing Context To Reuse
*   **Auth:** Clerk middleware and `useUser`/`useAuth` hooks.
*   **Database:** Existing Supabase schema and TypeScript types.
*   **UI Components:** Shared `Button`, `Input`, or `Card` components if already defined.
*   **Motion:** Lenis/GSAP configuration for smooth scrolling.

## Required Changes
*   **Directories:** Create specific feature folders in `src/components/features/...` and `src/app/api/...`.
*   **Environment Variables:** Add necessary keys for OpenAI/OpenRouter or Razorpay if required by this specific task.
*   **Schema:** Update Supabase tables or Pinecone namespaces if the task involves data persistence.

## Step-by-Step Execution Plan

### Phase 1: Foundation & Data Layer
1.  **Branch Setup:** Checkout to `develop` and create a feature branch: `feat/task-title`.
2.  **Database Schema (if applicable):** Create migrations in Supabase for any new tables. Run `supabase gen types` to update local TypeScript interfaces.
3.  **Server Actions/API:** Implement the core business logic in `src/lib/actions/` or `src/app/api/`. Ensure all Clerk `auth()` checks are performed first.
4.  **Unit Tests:** Create `*.test.ts` files using Vitest to verify the server-side logic and validation schemas.

### Phase 2: Premium UI Development
5.  **Component Scaffolding:** Build modular React components using Tailwind CSS. Follow the "Strong Typography Hierarchy" requirement.
6.  **Integration:** Connect UI components to the Server Actions/API logic using `react-hook-form` and `zod` for validation.
7.  **Motion Design:** 
    *   Implement GSAP for entrance animations.
    *   Apply Framer Motion for micro-interactions (e.g., premium button hover effects).
    *   Ensure Lenis smooth scroll remains uninterrupted.

### Phase 3: Integration & Security
8.  **Third-Party Integration:** Connect n8n automations or OpenAI/OpenRouter endpoints if the task requires AI/automation logic.
9.  **Payments/Monetization:** If the task involves checkout, implement server-side Razorpay verification.
10. **Security Audit:** Review code for exposed API keys. Ensure all sensitive logic is strictly server-side. Run a vulnerability scan.

### Phase 4: Observability & Quality Assurance
11. **Analytics:** Tag key interactions with PostHog events.
12. **Monitoring:** Verify Sentry is capturing potential errors in the new components.
13. **Responsive Review:** Audit UI on mobile, tablet, and desktop breakpoints.

## Testing Plan

### White Box (Logic & State)
*   **Tool:** Vitest + RTL.
*   **Focus:** Test state transitions, input validation, and API response handling.
*   **Coverage:** 100% of core business logic within this task.

### Black Box (User Flow)
*   **Tool:** Playwright.
*   **Focus:** End-to-end flow from authentication to task completion.
*   **Scenarios:** Success path, failure path (e.g., network error), and unauthorized access attempt.

### Manual Checks
*   **UI Polish:** Verify motion feels "premium" and not "heavy."
*   **Lighthouse:** Run a local audit to check for Performance/LCP issues.

## Risks
*   **Performance:** Heavy Three.js or GSAP animations could lower Lighthouse scores. *Mitigation: Use lazy loading and optimized assets.*
*   **Security:** Accidental exposure of Supabase service roles. *Mitigation: Strict linting and manual PR review.*
*   **Complexity:** Over-engineering the modular structure. *Mitigation: Follow the DRY principle but prioritize readability.*

## Definition of Done
- [ ] Code is modular, documented, and follows production-grade architecture.
- [ ] UI matches the "Premium" requirement with GSAP/Motion design.
- [ ] All Vitest and Playwright tests pass in the local environment.
- [ ] Server-side security checks for Auth and Payments are implemented.
- [ ] PostHog/Sentry integration is verified.
- [ ] Vulnerability scan shows no high-risk issues.
- [ ] Task is deployable on Vercel without build errors.
- [ ] Branch `feat/task-title` is merged into `develop`.  ## Execution Rules - Inspect existing code first - Do not rebuild blindly - Reuse existing logic where possible - Implement only this task - Test before completing - Work only on the target branch - Do not move to the next phase automatically unless the current phase is complete  ## Acceptance Criteria [] 