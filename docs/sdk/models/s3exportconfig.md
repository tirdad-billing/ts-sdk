# S3ExportConfig

## Example Usage

```typescript
import { S3ExportConfig } from "@tirdad-ai/sdk/sdk/models";

let value: S3ExportConfig = {};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `bucket`                                                               | *string*                                                               | :heavy_minus_sign:                                                     | S3 bucket name                                                         |
| `compression`                                                          | [models.S3CompressionType](../../sdk/models/s3compressiontype.md)      | :heavy_minus_sign:                                                     | N/A                                                                    |
| `encryption`                                                           | [models.S3EncryptionType](../../sdk/models/s3encryptiontype.md)        | :heavy_minus_sign:                                                     | N/A                                                                    |
| `isTirdadManaged`                                                   | *boolean*                                                              | :heavy_minus_sign:                                                     | If true, use Tirdad-managed S3 credentials instead of user-provided |
| `keyPrefix`                                                            | *string*                                                               | :heavy_minus_sign:                                                     | Optional prefix for S3 keys (e.g., "tirdad-exports/")               |
| `region`                                                               | *string*                                                               | :heavy_minus_sign:                                                     | AWS region (e.g., "us-west-2")                                         |