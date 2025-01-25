# Next.js 15 App Router Race Condition

This repository demonstrates a potential race condition bug in Next.js 15's App Router when fetching data concurrently from multiple routes.  The `profile.js` file shows how parallel data fetching from `/api/user` and `/api/posts` can lead to inconsistencies if these data sources interact in unexpected ways.

The solution (`profileSolution.js`) shows a simple approach to mitigating this by ensuring data fetching happens serially, or using techniques like optimistic updates and error handling to prevent inconsistent states.