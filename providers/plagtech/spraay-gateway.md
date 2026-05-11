---
name: spraay-gateway
title: "Spraay x402 Gateway"
description: "Full-stack pay-per-call crypto infrastructure with 88+ x402 endpoints across 19 categories covering batch payments on 15 chains, AI inference with 200+ models, Bittensor decentralized AI, DeFi, escrow, agent wallets, robotics, supply chain, GPU compute, and web search."
use_case: "Use for batch crypto payments, AI inference without API keys, on-chain escrow, agent wallet provisioning, robot task dispatch, supply chain automation, cross-chain bridge quotes, crypto tax calculation, and multi-chain RPC access."
category: finance
service_url: https://gateway.spraay.app
version: v3
endpoints:
  - method: POST
    path: api/v1/kyc/verify
    description: "Initiate KYC or KYB verification for compliance-gated payments and return verification status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.08
  - method: GET
    path: api/v1/kyc/status
    description: "Check KYC verification status for a previously submitted verification request"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: POST
    path: api/v1/auth/session
    description: "Create authenticated session with scoped permissions for subsequent gated requests"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: GET
    path: api/v1/auth/verify
    description: "Verify session token validity and check granted permissions for the current session"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/oracle/prices
    description: "Retrieve multi-token price feed with current spot prices across supported assets"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.008
  - method: GET
    path: api/v1/oracle/gas
    description: "Retrieve current gas prices on Base for transaction cost estimation"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/oracle/fx
    description: "Retrieve stablecoin FX rates for cross-denomination payment calculations"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.008
  - method: GET
    path: api/v1/analytics/wallet
    description: "Retrieve wallet profile including balance summary and activity overview for any address"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: GET
    path: api/v1/analytics/txhistory
    description: "Retrieve transaction history for any wallet address with pagination and filtering"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.008
  - method: GET
    path: api/v1/prices
    description: "Retrieve live token prices for supported assets across multiple chains"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/balances
    description: "Retrieve token balances for a wallet address across supported chains"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/resolve
    description: "Resolve ENS names and Basenames to wallet addresses and reverse-resolve addresses"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/chat/completions
    description: "Generate AI chat completions via 200+ models with OpenAI-compatible request format"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.04
  - method: GET
    path: api/v1/models
    description: "List all available AI models with capabilities and pricing metadata"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: POST
    path: api/v1/inference/classify-address
    description: "Classify a wallet address using AI with risk scoring and behavioral labels"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: POST
    path: api/v1/inference/classify-tx
    description: "Classify a transaction using AI with risk scoring and category identification"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: POST
    path: api/v1/inference/explain-contract
    description: "Analyze a smart contract using AI and return human-readable explanation of behavior"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: POST
    path: api/v1/inference/summarize
    description: "Generate AI intelligence briefing for any wallet address or transaction hash"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: GET
    path: bittensor/v1/models
    description: "List all available Bittensor AI models in OpenAI-compatible format for drop-in use"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: POST
    path: bittensor/v1/chat/completions
    description: "Generate chat completions via Bittensor decentralized AI with 43+ models including DeepSeek and Llama"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: POST
    path: bittensor/v1/images/generations
    description: "Generate images via Bittensor Subnet 19 using OpenAI-compatible image generation format"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.05
  - method: POST
    path: bittensor/v1/embeddings
    description: "Generate text embeddings via Bittensor for RAG pipelines and semantic search"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/notify/email
    description: "Send email notification for payment confirmations, alerts, and receipts"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: POST
    path: api/v1/notify/sms
    description: "Send SMS notification for payment alerts and transaction confirmations"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: GET
    path: api/v1/notify/status
    description: "Check delivery status for a previously sent email or SMS notification"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/webhook/register
    description: "Register a webhook URL for payment, escrow, and swap event notifications"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: POST
    path: api/v1/webhook/test
    description: "Send a test event to a registered webhook to verify connectivity and format"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/webhook/list
    description: "List all registered webhooks with their event types and delivery status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/webhook/delete
    description: "Delete a registered webhook by ID and stop all future event deliveries"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/xmtp/send
    description: "Send an encrypted XMTP message to any Ethereum address for agent-to-agent comms"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: GET
    path: api/v1/xmtp/inbox
    description: "Read XMTP inbox messages for an Ethereum address with pagination support"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: GET
    path: api/v1/swap/quote
    description: "Get swap quotes via Uniswap V3 with price impact and route information"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.008
  - method: GET
    path: api/v1/swap/tokens
    description: "List all supported tokens for swap operations with contract addresses"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: POST
    path: api/v1/swap/execute
    description: "Execute a token swap via Uniswap V3 and return the settlement transaction"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.015
  - method: GET
    path: api/v1/bridge/quote
    description: "Get cross-chain bridge quote with estimated fees and transfer time"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.05
  - method: GET
    path: api/v1/bridge/chains
    description: "List supported bridge chains with token and route availability"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/payroll/execute
    description: "Execute batch payroll via Spraay V2 contracts for multiple recipients in one transaction"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.10
  - method: POST
    path: api/v1/payroll/estimate
    description: "Estimate total payroll costs including gas and protocol fees before execution"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.003
  - method: GET
    path: api/v1/payroll/tokens
    description: "List supported payroll stablecoins with chain availability and decimals"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/invoice/create
    description: "Create a crypto invoice with payment transaction details and expiry"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.05
  - method: GET
    path: api/v1/invoice/list
    description: "List invoices by wallet address with status filtering and pagination"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: GET
    path: api/v1/invoice/:id
    description: "Retrieve invoice details by ID including payment status and transaction hash"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: POST
    path: api/v1/escrow/create
    description: "Create conditional escrow with milestones, arbiter, and expiry for trustless payments"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.10
  - method: GET
    path: api/v1/escrow/list
    description: "List escrows by wallet address with status and role filtering"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: GET
    path: api/v1/escrow/:id
    description: "Retrieve escrow details by ID including milestones and current status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/escrow/fund
    description: "Mark an escrow as funded after the depositor has sent the required amount"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/escrow/release
    description: "Release escrow funds to the recipient and return the unsigned transfer transaction"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.08
  - method: POST
    path: api/v1/escrow/cancel
    description: "Cancel an active escrow and trigger refund to the depositor address"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/batch/execute
    description: "Execute batch payments to multiple recipients across 15 chains in one transaction"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/batch/estimate
    description: "Estimate gas costs for a batch payment before execution across supported chains"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: POST
    path: api/v1/rpc/call
    description: "Execute premium multi-chain RPC call via Alchemy or Helius infrastructure"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: GET
    path: api/v1/rpc/chains
    description: "List supported RPC chains with available methods and endpoint status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: POST
    path: api/v1/storage/pin
    description: "Pin content to IPFS or Arweave for permanent decentralized storage"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: GET
    path: api/v1/storage/get
    description: "Retrieve pinned content by CID from IPFS or Arweave permanent storage"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/storage/status
    description: "Check pin status and replication progress for content stored on IPFS"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/cron/create
    description: "Create a scheduled job for recurring payments, DCA orders, or timed reminders"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.01
  - method: GET
    path: api/v1/cron/list
    description: "List all scheduled jobs with next execution time and status information"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/cron/cancel
    description: "Cancel a scheduled job by ID and stop all future executions permanently"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/logs/ingest
    description: "Ingest structured log entries for debugging and monitoring agent workflows"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: GET
    path: api/v1/logs/query
    description: "Query structured logs by service name, severity level, and time range"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/audit/log
    description: "Record immutable audit trail entry for payments, escrows, and compliance events"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/audit/query
    description: "Query audit trail by actor, action type, resource, and time range with filters"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: POST
    path: api/v1/gpu/run
    description: "Run AI model inference via Replicate GPU for image, video, audio, and LLM tasks"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.06
  - method: GET
    path: api/v1/gpu/status/:id
    description: "Check prediction status for asynchronous GPU compute jobs by prediction ID"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/search/web
    description: "Search the web and return clean LLM-ready results via Tavily with configurable depth"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/search/extract
    description: "Extract clean structured content from up to 5 URLs for RAG pipeline ingestion"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/search/qna
    description: "Answer questions by searching the web and synthesizing a response with source citations"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: POST
    path: api/v1/robots/task
    description: "Dispatch a paid task to an RTP-registered robot with x402 payment held in escrow"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.05
  - method: GET
    path: api/v1/robots/list
    description: "Discover available RTP robots filtered by capability, chain, price, and status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: GET
    path: api/v1/robots/status
    description: "Poll RTP task status including PENDING, IN_PROGRESS, COMPLETED, and FAILED states"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: GET
    path: api/v1/robots/profile
    description: "Retrieve full RTP robot profile with capabilities, pricing, and connection details"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: POST
    path: api/v1/robots/register
    description: "Register a new robot in the RTP directory with capabilities and pricing configuration"
  - method: POST
    path: api/v1/robots/complete
    description: "Report robot task completion result which triggers escrow release or refund"
  - method: PATCH
    path: api/v1/robots/update
    description: "Update registered robot name, capabilities, pricing, or connection configuration"
  - method: POST
    path: api/v1/robots/deregister
    description: "Remove a robot from the RTP registry, blocked if the robot has active tasks"
  - method: POST
    path: api/v1/sctp/supplier
    description: "Register a supplier in the SCTP directory with contact and capability metadata"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: GET
    path: api/v1/sctp/supplier/:id
    description: "Retrieve supplier details by ID including capabilities and contact information"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/sctp/po
    description: "Create a purchase order with line items, quantities, and supplier assignment"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: GET
    path: api/v1/sctp/po/:id
    description: "Retrieve purchase order details including line items and fulfillment status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/sctp/invoice
    description: "Submit an invoice linked to a purchase order for verification and payment"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: GET
    path: api/v1/sctp/invoice/:id
    description: "Retrieve invoice details including linked purchase order and payment status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/sctp/invoice/verify
    description: "Verify an invoice against its purchase order using AI and return match score"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.03
  - method: POST
    path: api/v1/sctp/pay
    description: "Execute supplier payment for a verified invoice via batch settlement on Base"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.10
  - method: POST
    path: api/v1/agent-wallet/provision
    description: "Deploy an ERC-4337 smart contract wallet for an AI agent on Base mainnet"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.05
  - method: POST
    path: api/v1/agent-wallet/session-key
    description: "Add a session key with spending limits and time bounds to an agent wallet"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: GET
    path: api/v1/agent-wallet/info
    description: "Retrieve agent wallet info including balance, metadata, and active session keys"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/agent-wallet/revoke-key
    description: "Revoke an active session key immediately and invalidate all pending authorizations"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: GET
    path: api/v1/agent-wallet/predict
    description: "Predict agent wallet contract address before deployment using CREATE2 derivation"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: GET
    path: api/v1/wallet/list
    description: "List provisioned agent wallets with pagination and status filtering"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.002
  - method: GET
    path: api/v1/wallet/:walletId
    description: "Retrieve agent wallet details including chain addresses and signing status"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: GET
    path: api/v1/wallet/:walletId/addresses
    description: "Retrieve chain-specific addresses for a provisioned agent wallet"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: POST
    path: api/v1/wallet/sign-message
    description: "Sign an arbitrary message with an agent wallet for authentication or verification"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.005
  - method: POST
    path: api/v1/wallet/send-transaction
    description: "Sign and broadcast a transaction from an agent wallet to any supported chain"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/wallet/create
    description: "Create a new keyed agent wallet with server-side signing for rapid prototyping"
  - method: POST
    path: api/v1/xrp/batch
    description: "Execute batch XRP payments to multiple recipients on the XRP Ledger"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/xrp/estimate
    description: "Estimate total cost for an XRP batch payment including network fees"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: GET
    path: api/v1/xrp/info
    description: "Retrieve XRP Ledger chain info including fee address and supported features"
  - method: POST
    path: api/v1/stellar/batch
    description: "Execute batch XLM payments to multiple recipients on the Stellar network"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.02
  - method: POST
    path: api/v1/stellar/estimate
    description: "Estimate total cost for a Stellar batch payment including network fees"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.001
  - method: POST
    path: api/v1/tax/calculate
    description: "Calculate crypto tax gain and loss using FIFO method across transaction history"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.08
  - method: GET
    path: api/v1/tax/report
    description: "Retrieve formatted tax report with IRS Form 8949-compatible data and totals"
    pricing:
      dimensions:
        - direction: usage
          unit: requests
          scale: 1
          tiers:
            - price_usd: 0.05
---

## Usage Notes

All endpoints return HTTP 402 with x402 payment challenge headers. Settlement is USDC on Base via the Coinbase x402 facilitator. Payments settle to `0xAd62f03C7514bb8c51f1eA70C2b75C37404695c8`.

Bittensor endpoints (`/bittensor/v1/*`) are OpenAI-compatible drop-ins — use the same request format as OpenAI and just change the base URL.

AI Inference covers 200+ models via `/api/v1/chat/completions`. Bittensor covers 43+ decentralized models separately via `/bittensor/v1/chat/completions`.

Free endpoints (robot registration, wallet creation, chain info) require no payment.

## Spend-Aware Usage

- Use data read endpoints ($0.001–$0.01) before write operations ($0.02–$0.10).
- Use `/api/v1/batch/estimate` before `/api/v1/batch/execute` to preview costs.
- Use `/api/v1/escrow/create` only after confirming terms — escrow creation is $0.10.
- Prefer `/api/v1/prices` ($0.005) over `/api/v1/oracle/prices` ($0.008) for simple price lookups.
- Ask before executing payroll, escrow, bridge, or swap operations as these involve real fund movement.
