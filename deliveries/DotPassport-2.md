# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/DotPassport.md
* **Milestone Number:** 2
* **DOT Payment Address:** 15MKh6ZjeKkRqz46gcMxEK9yLXpqhjzRYVKqK7dPg5UE2YA9

**Context**

Milestone 2 delivers the **dApp SDK + REST API + Developer Docs** and **Wallet Integration** as promised in the grant application. This includes a TypeScript SDK published to NPM, 4 embeddable widgets, a Developer API (v2) with API key authentication and rate limiting, a Sandbox testing platform, and comprehensive documentation.

**Live Platforms:**
- Main App: https://dotpassport.io
- Developer Sandbox: https://sandbox.dotpassport.io
- Documentation: https://docs.dotpassport.io
- NPM Package: https://www.npmjs.com/package/@dotpassport/sdk
- GitHub: https://github.com/SachinCoder1/DotPassport

**Deliverables**

| Number | Deliverable | Link | Notes |
| --- | --- | --- | --- |
| 0a. | License | [LICENSE](https://github.com/SachinCoder1/DotPassport/blob/317b80c/LICENSE) | MIT |
| 0b. | Documentation | SDK README: [sdk/README.md](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/README.md) · Full Docs: https://docs.dotpassport.io · API Reference: [api-reference.md](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/docs/api-reference.md) | Comprehensive SDK documentation with 44+ markdown files covering getting started, API reference, widgets, framework integration (React, Vue, Angular, Svelte), wallet guides, and examples |
| 0c. | Testing & Guide | Backend tests: [backend/src tests](https://github.com/SachinCoder1/DotPassport/tree/317b80c/backend/src) · SDK tests: [sdk/src/\_\_tests\_\_](https://github.com/SachinCoder1/DotPassport/tree/317b80c/sdk/src/__tests__) · Widget tests: [widgets/\_\_tests\_\_](https://github.com/SachinCoder1/DotPassport/tree/317b80c/sdk/src/widgets/__tests__) | **27 test files total**: 17 backend tests (303+ passing) covering API routes, services, middleware + 10 SDK tests covering client API, all 4 widgets, factory, integration, utilities, and templates |
| 0d. | Article | [Milestone 2 Article](https://dotpassport.io/blog/dotpassport-m2) · Source: [page.tsx](https://github.com/SachinCoder1/DotPassport/blob/317b80c/client/src/app/blog/dotpassport-m2/page.tsx) | Overview of SDK, widgets, Sandbox platform, and developer integration |
| 3a. | **dApp SDK** | SDK source: [sdk/src/client.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/src/client.ts) · Types: [sdk/src/types.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/src/types.ts) · NPM: [@dotpassport/sdk](https://www.npmjs.com/package/@dotpassport/sdk) | TypeScript SDK with 7 API methods: `getProfile()`, `getScores()`, `getCategoryScore()`, `getBadges()`, `getBadge()`, `getBadgeDefinitions()`, `getCategoryDefinitions()`. Features include built-in caching, error handling, AbortSignal support. |
| 3b. | **REST API v2** | Routes: [developerRoutes.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/backend/src/developer/routes/developerRoutes.ts) · Controller: [developerController.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/backend/src/developer/controller/developerController.ts) · Widget Endpoint: [widgetController.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/backend/src/developer/controller/widgetController.ts) | 7 public API endpoints with API key authentication (`X-API-Key` header), tiered rate limiting (FREE: 100/hr, PRO: 1000/hr), CORS validation, and request logging |
| 3c. | **Developer Docs** | Docs site: https://docs.dotpassport.io · Source: [sdk/docs/](https://github.com/SachinCoder1/DotPassport/tree/317b80c/sdk/docs) | 44+ markdown files covering: installation, quick start, API client reference, widget documentation (4 widgets), framework integration (React, Vue, Angular, Svelte, Vanilla JS), wallet guides (Talisman, SubWallet), advanced topics (caching, security, performance) |
| 4a. | **Wallet Integration** | Wallet Connect: [PolkadotWalletConnect.tsx](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sandbox/src/components/PolkadotWalletConnect.tsx) · Wallet Store: [walletStore.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sandbox/src/store/walletStore.ts) · Auth Service: [authService.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sandbox/src/service/authService.ts) | Full Polkadot wallet integration supporting **Talisman**, **SubWallet**, and **Polkadot.js Extension**. Challenge-response authentication with wallet signature. Account persistence and session management. |
| 4b. | **Embeddable Widgets** | Widget Factory: [widgets/index.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/src/widgets/index.ts) · ReputationWidget: [ReputationWidget.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/src/widgets/ReputationWidget.ts) · BadgeWidget: [BadgeWidget.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/src/widgets/BadgeWidget.ts) · ProfileWidget: [ProfileWidget.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/src/widgets/ProfileWidget.ts) · CategoryWidget: [CategoryWidget.ts](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sdk/src/widgets/CategoryWidget.ts) | 4 ready-to-use embeddable widgets with Light/Dark/Auto themes, CSS variable customization, and lifecycle management (mount, update, destroy, refresh) |
| 4c. | **Sandbox Platform** | Live: https://sandbox.dotpassport.io · Dashboard: [DashboardPage.tsx](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sandbox/src/pages/DashboardPage.tsx) · API Testing: [ApiTestingPage.tsx](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sandbox/src/pages/ApiTestingPage.tsx) · Widget Playground: [WidgetTestingPage.tsx](https://github.com/SachinCoder1/DotPassport/blob/317b80c/sandbox/src/pages/WidgetTestingPage.tsx) | Interactive developer sandbox with: Dashboard (API key management, usage stats), API Testing (test all 7 methods with live responses), Widget Playground (preview & customize all 4 widgets), Request Logs tracking |

**Additional Information**

**SDK Features:**
- Published to NPM as `@dotpassport/sdk`
- TypeScript-first with full type definitions
- Tree-shakeable widget exports
- Built-in 5-minute global cache for widget data
- Axios-based HTTP client with standardized error handling
- Environment configuration (local, staging, production)

**API v2 Features:**
- 7 endpoints: profiles, scores, category scores, badges, specific badge, badge metadata, category metadata
- Consolidated widget endpoints (`/api/v2/widget/:type/:address`) for optimized frontend performance
- API key authentication with SHA-256 hashing
- Tiered rate limiting with automatic window resets
- Request logging for usage analytics
- CORS validation with wildcard subdomain support

**Widget System:**
- 4 widgets: Reputation, Badge, Profile, Category
- Light/Dark/Auto theme support
- CSS variables for custom styling
- Abstract BaseWidget class for consistent lifecycle
- Event callbacks (onLoad, onError, onUpdate)

**Wallet Support:**
- Talisman Wallet
- SubWallet
- Polkadot.js Extension
- Challenge-response authentication pattern
- Session persistence with JWT tokens

**Test Coverage:**
- **27 test files total** with comprehensive coverage
- Backend: 17 test files, 303+ passing tests (API routes, services, middleware, integrations)
- SDK: 10 test files covering client API, all 4 widgets, widget factory, integration tests, utilities, and templates
- Jest with MongoDB Memory Server for isolated backend testing
- Vitest for SDK testing with DOM mocking

**Documentation:**
- 44+ markdown files
- Framework guides: React, Vue, Angular, Svelte, Vanilla JS
- Wallet integration guides: Talisman, SubWallet
- Complete API reference with examples
- Advanced topics: caching, security, performance, error recovery

---

## Screenshots

### Embeddable Widgets

<table>
  <tr>
    <td align="center">
      <img src="https://i.ibb.co/bMmjMXp2/dotpassport-profile-widget.png" width="200" alt="Profile Widget"/>
      <br/>
      <b>Profile Widget</b>
    </td>
    <td align="center">
      <img src="https://i.ibb.co/fVxDyQFJ/dotpassport-reputation-widget-light.png" width="200" alt="Reputation Widget (Light)"/>
      <br/>
      <b>Reputation Widget</b>
    </td>
    <td align="center">
      <img src="https://i.ibb.co/Wp7Q7408/dotpassport-badge-widget-light.png" width="200" alt="Badge Widget"/>
      <br/>
      <b>Badge Widget</b>
    </td>
    <td align="center">
      <img src="https://i.ibb.co/chgG04Ws/dotpassport-reputation-widget-dark.png" width="200" alt="Reputation Widget (Dark)"/>
      <br/>
      <b>Dark Mode Support</b>
    </td>
  </tr>
</table>

### Developer Sandbox

<table>
  <tr>
    <td align="center">
      <img src="https://i.ibb.co/wZc8GRWG/dotpassport-sandbox-dashboard.png" width="600" alt="Sandbox Dashboard"/>
      <br/>
      <b>Dashboard</b> - API key management, usage stats, rate limit tracking
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://i.ibb.co/N61MmCDY/dotpassport-sandbox-api-testing-page.png" width="600" alt="API Testing Page"/>
      <br/>
      <b>API Testing</b> - Test all 7 endpoints with live responses
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://i.ibb.co/B5PHBQfq/dotpassport-widget-testing-page.png" width="600" alt="Widget Playground"/>
      <br/>
      <b>Widget Playground</b> - Live preview and customize all 4 widgets
    </td>
  </tr>
</table>
