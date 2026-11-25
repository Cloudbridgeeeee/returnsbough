# ReturnsBough — proposed AWS architecture

ReturnsBough uses AWS to understand return reasons in customers’ own words, find patterns and forecast volumes — securely for each retailer.

## Request flow

1. Return records
2. Amazon S3
3. AWS Lambda
4. Bedrock
5. SageMaker AI
6. DynamoDB
7. Team review

## Services

### Amazon Bedrock

**Role:** Understand return comments

Classifies free-text return comments into reason families, extracts details like “runs small” or “colour differs from photo”, and drafts merchandising suggestions for review.

### Amazon SageMaker AI

**Role:** Forecast and cluster returns

Forecasts return volumes by category and clusters similar complaints to uncover product defects and supplier issues.

### Amazon S3

**Role:** Store return history

Keeps return, order and catalogue exports encrypted as the history that analysis and forecasts are built on.

### Amazon DynamoDB

**Role:** Serve products and insights

Stores classified returns, product insights, suggested actions and approvals for fast dashboard access.

### AWS Lambda

**Role:** Link and process returns

Links returns to orders, SKUs and warehouses, triggers classification and refreshes insights as new returns arrive.

## Principles

- **Product, not person** — Analysis focuses on products and orders, not individual shoppers.
- **Comments respected** — Customer words are summarised faithfully, with examples.
- **Measured fixes** — Every approved action is tracked for impact.

## Safeguards

- **Teams decide** — Suggested catalogue and process changes are reviewed by your merchandisers and ops teams.
- **Shopper privacy** — Customer names and contact details are removed on import; only product and order data is analysed.
- **Evidence attached** — Every insight links to example return comments.
- **No refund decisions** — ReturnsBough analyses returns; it never approves or denies refunds.

## MVP scope

We import six to twelve months of return records with comments, classify every one, and deliver product-level analytics and a prioritised list of fixes your teams review.

- Return record import
- Reason classification
- Product and size analytics
- Fulfilment error tracking
- Prioritised fix list
