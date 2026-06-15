# Branch GraphQL API

Branch's Quote to Bind GraphQL API exposes everything an affinity partner needs to go from initial quote to final purchase of Branch home + auto (and optional umbrella) insurance without leaving their platform. Partners authenticate with an API key in the Authorization header and (when acting on behalf of multiple agencies) an x-affinity-code header. The typical end-to-end flow is requestQuoteV2 -> recalculateQuoteV2 / addCar / addDriver -> requestBind, after which the offer becomes a bound policy retrievable via getBoundPoliciesByOfferId and getPolicyDocuments. Offers are immutable — any modification produces a new offer ID, and all prior versions remain queryable via getOffer. Partners may complete the entire purchase flow via the API or hand the customer off to ourbranch.com at any step (customize, review, checkout, sign-documents) and retain attribution. Policy-bound and documents-signed notifications are offered via webhook (instant) or scheduled CSV reporting to SFTP / S3. "Enhanced" calls (enhancedGetOffer etc.) return additional data such as driver date of birth and require enhanced-data access. A staging endpoint at https://staging.v2.api.ourbranch.com mirrors production with a shared test-user universe.

**Endpoint:** https://api.ourbranch.com/

**Documentation:** https://docs.v2.api.ourbranch.com/

**References:**

- Documentation: https://docs.v2.api.ourbranch.com/
- Documentation: https://docs.v2.api.ourbranch.com/request-quote-v2
- Documentation: https://docs.v2.api.ourbranch.com/recalculate-quote-v2
