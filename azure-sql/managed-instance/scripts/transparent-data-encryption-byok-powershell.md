---
title: Use PowerShell to enable transparent data encryption
titleSuffix: Azure SQL Managed Instance
description: Enable transparent data encryption in Azure SQL Managed Instance using PowerShell and your own key.
author: MladjoA
ms.author: mlandzic
ms.reviewer: vanto
ms.date: 05/18/2022
ms.service: sql-managed-instance
ms.subservice: security
ms.topic: conceptual
ms.custom: kr2b-contr-experiment
ms.devlang: powershell
---

# PowerShell script to enable transparent data encryption using your own key

[!INCLUDE[appliesto-sqldb](../../includes/appliesto-sqlmi.md)]

This PowerShell script example configures transparent data encryption (TDE) in Azure SQL Managed Instance, using a customer-managed key from Azure Key Vault. This is often referred to as a bring-your-own-key (BYOK) scenario for TDE. To learn more, see [Azure SQL Transparent Data Encryption with customer-managed key](../../database/transparent-data-encryption-byok-overview.md).

## Prerequisites

- An existing managed instance. See [Use PowerShell to create a managed instance](create-configure-managed-instance-powershell.md).

[!INCLUDE [quickstarts-free-trial-note](../../includes/quickstarts-free-trial-note.md)]
[!INCLUDE [updated-for-az](../../includes/updated-for-az.md)]
[!INCLUDE [cloud-shell-try-it.md](../../includes/cloud-shell-try-it.md)]

Using PowerShell locally or using Azure Cloud Shell requires Azure PowerShell 2.3.2 or a later version. If you need to upgrade, see [Install Azure PowerShell module](/powershell/azure/install-az-ps), or run the below sample script to install the module for the current user:

`Install-Module -Name Az -AllowClobber -Scope CurrentUser`

If you are running PowerShell locally, you also need to run `Connect-AzAccount` to create a connection with Azure.

## Sample scripts 

[!code-powershell-interactive[main](~/../powershell_scripts/sql-database/transparent-data-encryption/setup-tde-byok-sqlmi.ps1 "Set up BYOK TDE for SQL Managed Instance")]

## Next steps

For more information on Azure PowerShell, see [Azure PowerShell documentation](/powershell/azure/).

Additional PowerShell script samples for SQL Managed Instance can be found in [Azure SQL Managed Instance PowerShell scripts](../../database/powershell-script-content-guide.md).
