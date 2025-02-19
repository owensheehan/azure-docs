---
title: Blob storage features available in Azure Data Lake Storage Gen2 | Microsoft Docs
description: Learn about which Blob storage features you can use with Azure Data Lake Storage Gen2
author: normesta
ms.subservice: data-lake-storage-gen2
ms.service: storage
ms.topic: conceptual
ms.date: 06/29/2021
ms.author: normesta
---

# Blob storage features available in Azure Data Lake Storage Gen2

Blob Storage features such as [diagnostic logging](../common/storage-analytics-logging.md), [access tiers](storage-blob-storage-tiers.md), and [Blob Storage lifecycle management policies](storage-lifecycle-management-concepts.md) now work with accounts that have a hierarchical namespace. Therefore, you can enable hierarchical namespaces on your Blob storage accounts without losing access to these features.

This table lists the Blob storage features that you can use with Azure Data Lake Storage Gen2. The items that appear in these tables will change over time as support continues to expand. To learn more about specific issues associated with the preview status of a feature, see the [Known issues](data-lake-storage-known-issues.md) article.

## Supported Blob storage features

The following table shows how each Blob storage feature is supported with Data Lake Storage Gen2. There's a column for standard and [premium performance](premium-tier-for-data-lake-storage.md) tiers. 

|Blob Storage feature |Standard |Premium |Related articles |
|---------------|-------------------|---|
|Hot access tier|Generally available|Not supported|[Azure Blob storage: hot, cool, and archive access tiers](storage-blob-storage-tiers.md)|
|Cool access tier|Generally available|Not supported|[Azure Blob storage: hot, cool, and archive access tiers](storage-blob-storage-tiers.md)|
|Events|Generally available|Generally available|[Reacting to Blob storage events](storage-blob-event-overview.md)|
|Metrics (Classic)|Generally available|Generally available|[Azure Storage analytics metrics (Classic)](../common/storage-analytics-metrics.md?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)|
|Metrics in Azure Monitor|Generally available|Preview|[Azure Storage metrics in Azure Monitor](./monitor-blob-storage.md?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)|
|Blob storage PowerShell commands|Generally available|Generally available|[Quickstart: Upload, download, and list blobs with PowerShell](storage-quickstart-blobs-powershell.md)|
|Blob storage Azure CLI commands|Generally available|Generally available|[Quickstart: Create, download, and list blobs with Azure CLI](storage-quickstart-blobs-cli.md)|
|Blob storage APIs|Generally available|Generally available|[Quickstart: Azure Blob storage client library v12 for .NET](storage-quickstart-blobs-dotnet.md)<br>[Quickstart: Manage blobs with Java v12 SDK](storage-quickstart-blobs-java.md)<br>[Quickstart: Manage blobs with Python v12 SDK](storage-quickstart-blobs-python.md)<br>[Quickstart: Manage blobs with JavaScript v12 SDK in Node.js](storage-quickstart-blobs-nodejs.md)|
|Customer-managed keys|Generally available|Generally available|[Customer-managed keys for Azure Storage encryption](../common/customer-managed-keys-overview.md?toc=/azure/storage/blobs/toc.json)|
|Diagnostic logs|Generally available|Preview |[Azure Storage analytics logging](../common/storage-analytics-logging.md?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)|
|Archive Access Tier|Generally available|Not supported|[Azure Blob storage: hot, cool, and archive access tiers](storage-blob-storage-tiers.md)|
|Lifecycle management policies (tiering)|Generally available|Not yet supported|[Manage the Azure Blob storage lifecycle](storage-lifecycle-management-concepts.md)|
|Lifecycle management policies (delete blob)|Generally available|Generally available|[Manage the Azure Blob storage lifecycle](storage-lifecycle-management-concepts.md)|
|Container soft delete|Generally available|Generally available|[Soft delete for containers](soft-delete-container-overview.md)|
|Logging in Azure Monitor|Preview |Preview|[Monitoring Azure Storage](./monitor-blob-storage.md)|
|Snapshots|Preview|Preview|[Blob snapshots](snapshots-overview.md)|
|Static websites|Generally Available<div role="complementary" aria-labelledby="preview-form"></div>|Generally Available<div role="complementary" aria-labelledby="preview-form"></div>|[Static website hosting in Azure Storage](storage-blob-static-website.md)|
|Immutable storage|Preview<div role="complementary" aria-labelledby="preview-form"><sup>1</sup></div>|Preview<div role="complementary" aria-labelledby="preview-form"><sup>1</sup></div>|[Store business-critical blob data with immutable storage](immutable-storage-overview.md)|
|Azure Storage inventory|Preview|Preview|[Use Azure Storage inventory to manage blob data (preview)](blob-inventory.md)|
|Custom domains|Preview<div role="complementary" aria-labelledby="preview-form-1"><sup>1</sup></div>|Preview<div role="complementary" aria-labelledby="preview-form-1"><sup>1</sup></div>|[Map a custom domain to an Azure Blob storage endpoint](storage-custom-domain-name.md)|
|Blob soft delete|Preview|Preview|[Soft delete for blobs](./soft-delete-blob-overview.md)|
|Blobfuse|Generally available|Generally available|[How to mount Blob storage as a file system with blobfuse](storage-how-to-mount-container-linux.md)|
|Anonymous public access |Generally available|Generally available| See [Configure anonymous public read access for containers and blobs](anonymous-read-access-configure.md).|
|Customer-managed account failover|Not yet supported|Not yet supported|[Disaster recovery and account failover](../common/storage-disaster-recovery-guidance.md?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)|
|Customer-provided keys|Not yet supported|Not yet supported|[Provide an encryption key on a request to Blob storage](encryption-customer-provided-keys.md)|
|Encryption scopes|Not yet supported|Not yet supported|[Create and manage encryption scopes](encryption-scope-manage.md)|
|Change feed|Not yet supported|Not yet supported|[Change feed support in Azure Blob storage](storage-blob-change-feed.md)|
|Object replication|Not yet supported|Not yet supported|[Configure object replication for block blobs](object-replication-configure.md)|
|Blob versioning|Not yet supported|Not yet supported|[Enable and manage blob versioning](versioning-enable.md)|
|Point-in-time restore|Not yet supported|Not yet supported|[Point-in-time restore for block blobs](point-in-time-restore-overview.md)|
|Blob index tags|Not yet supported|Not yet supported|[Manage and find Azure Blob data with blob index tags](storage-manage-find-blobs.md)|

<div id="preview-form-2"><sup>1</sup>A custom domain name can map only to the blob service or static website endpoint. The Data Lake storage endpoint is not supported.</a>.  </div>

## See also

- [Known issues with Azure Data Lake Storage Gen2](data-lake-storage-known-issues.md)
- [Azure services that support Azure Data Lake Storage Gen2](data-lake-storage-supported-azure-services.md)
- [Open source platforms that support Azure Data Lake Storage Gen2](data-lake-storage-supported-open-source-platforms.md)
- [Multi-protocol access on Azure Data Lake Storage](data-lake-storage-multi-protocol-access.md)
