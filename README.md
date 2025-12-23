# FinalBoss SDK

**Cryptographic Metering + Signed Reconciliation (PQC-Ready)**

---

## What This Is

I'm not billing you. I'm preventing you from overpaying.

I meter usage at the server-side decision point (ALLOW vs DENY), and I export a signed reconciliation bundle you can audit and dispute with confidence.

I also provide post-quantum receipt signing (**ML-DSA-65 / FIPS 204**) so you can keep your governance evidence future-resistant.

---

## Available via Evaluation License

| Platform | Distribution | Access |
|----------|--------------|--------|
| **Python SDK** | Wheel (.whl) | Provided on request |
| **NPM SDK** | Tarball (.tgz) | Provided on request |
| **REST API** | Sandbox + credentials | Provided on request |

---

## Capabilities

- **Server-Side Metering** - Meter at the ALLOW/DENY decision point. No client-side tampering possible.
- **Signed Reconciliation Bundles** - Export cryptographically signed usage records for audit and dispute resolution.
- **Post-Quantum Signatures** - ML-DSA-65 (NIST FIPS 204) for quantum-resistant governance evidence.
- **Hash-Chain Integrity** - Append-only receipt chain with tamper-evident linking.
- **Epoch-Based Revocation** - O(1) instant mass invalidation for security incidents.

---

## Quick Start

### Python

```python
from finalboss_idv import IDVClient

client = IDVClient(
    base_url="https://api.finalbosstech.com",
    client_id="your-client-id",
    client_secret="your-client-secret"
)

# Create verification
verification = client.create_verification(
    subject_id="user-123",
    verification_type="document"
)

# Get signed reconciliation bundle
bundle = client.export_reconciliation_bundle()
```

### Node.js / TypeScript

```typescript
import { IDVClient } from '@finalboss/idv-sdk';

const client = new IDVClient({
  clientId: 'your-client-id',
  clientSecret: 'your-client-secret'
});

// Create verification
const verification = await client.createVerification({
  user_id: 'user-123',
  verification_type: 'identity'
});

// Get PQC-signed receipts
const receipts = await client.exportPQCReceipts();
```

---

## Request Evaluation Access

**Email:** [ABRAHAM@FINALBOSSTECH.COM](mailto:ABRAHAM@FINALBOSSTECH.COM?subject=FinalBoss%20SDK%20Evaluation%20Request)

Include:
- Organization name
- Use case
- Deployment mode (cloud / on-prem / air-gapped)

---

## License

Available via evaluation license. Contact for commercial terms.

---

&copy; 2025 FinalBoss Technologies
