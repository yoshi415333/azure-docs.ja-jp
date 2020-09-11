---
title: リソースの種類別の移動操作のサポート
description: 新しいリソース グループまたはサブスクリプションに移動できる Azure リソースの種類を一覧表示します。
ms.topic: conceptual
ms.date: 07/13/2020
ms.openlocfilehash: 16197210326d73284a4a83edc7876e4faddded86
ms.sourcegitcommit: 3d79f737ff34708b48dd2ae45100e2516af9ed78
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2020
ms.locfileid: "87079511"
---
# <a name="move-operation-support-for-resources"></a>リソースの操作のサポートの移動

この記事では、Azure リソースの種類は、移動操作をサポートしているかどうかを示します。 また、リソースを移動するときに考慮すべき特別な条件に関する情報も提供します。

リソース プロバイダーの名前空間に移動します。
> [!div class="op_single_selector"]
> - [Microsoft.AAD](#microsoftaad)
> - [microsoft.aadiam](#microsoftaadiam)
> - [Microsoft.Addons](#microsoftaddons)
> - [Microsoft.ADHybridHealthService](#microsoftadhybridhealthservice)
> - [Microsoft.Advisor](#microsoftadvisor)
> - [Microsoft.AlertsManagement](#microsoftalertsmanagement)
> - [Microsoft.AnalysisServices](#microsoftanalysisservices)
> - [Microsoft.ApiManagement](#microsoftapimanagement)
> - [Microsoft.AppConfiguration](#microsoftappconfiguration)
> - [Microsoft.AppPlatform](#microsoftappplatform)
> - [Microsoft.AppService](#microsoftappservice)
> - [Microsoft.Attestation](#microsoftattestation)
> - [Microsoft.Authorization](#microsoftauthorization)
> - [Microsoft.Automation](#microsoftautomation)
> - [Microsoft.AVS](#microsoftavs)
> - [Microsoft.AzureActiveDirectory](#microsoftazureactivedirectory)
> - [Microsoft.AzureData](#microsoftazuredata)
> - [Microsoft.AzureStack](#microsoftazurestack)
> - [Microsoft.AzureStackHCI](#microsoftazurestackhci)
> - [Microsoft.Batch](#microsoftbatch)
> - [Microsoft.Billing](#microsoftbilling)
> - [Microsoft.BingMaps](#microsoftbingmaps)
> - [Microsoft.BizTalkServices](#microsoftbiztalkservices)
> - [Microsoft.Blockchain](#microsoftblockchain)
> - [Microsoft.BlockchainTokens](#microsoftblockchaintokens)
> - [Microsoft.Blueprint](#microsoftblueprint)
> - [Microsoft.BotService](#microsoftbotservice)
> - [Microsoft.Cache](#microsoftcache)
> - [Microsoft.Capacity](#microsoftcapacity)
> - [Microsoft.Cdn](#microsoftcdn)
> - [Microsoft.CertificateRegistration](#microsoftcertificateregistration)
> - [Microsoft.ChangeAnalysis](#microsoftchangeanalysis)
> - [Microsoft.ClassicCompute](#microsoftclassiccompute)
> - [Microsoft.ClassicInfrastructureMigrate](#microsoftclassicinfrastructuremigrate)
> - [Microsoft.ClassicNetwork](#microsoftclassicnetwork)
> - [Microsoft.ClassicStorage](#microsoftclassicstorage)
> - [Microsoft.ClassicSubscription](#microsoftclassicsubscription)
> - [Microsoft.CognitiveServices](#microsoftcognitiveservices)
> - [Microsoft.Commerce](#microsoftcommerce)
> - [Microsoft.Compute](#microsoftcompute)
> - [Microsoft.Consumption](#microsoftconsumption)
> - [Microsoft.ContainerInstance](#microsoftcontainerinstance)
> - [Microsoft.ContainerRegistry](#microsoftcontainerregistry)
> - [Microsoft.ContainerService](#microsoftcontainerservice)
> - [Microsoft.ContentModerator](#microsoftcontentmoderator)
> - [Microsoft.CortanaAnalytics](#microsoftcortanaanalytics)
> - [Microsoft.CostManagement](#microsoftcostmanagement)
> - [Microsoft.CostManagementExports](#microsoftcostmanagementexports)
> - [Microsoft.CustomerInsights](#microsoftcustomerinsights)
> - [Microsoft.CustomerLockbox](#microsoftcustomerlockbox)
> - [Microsoft.CustomProviders](#microsoftcustomproviders)
> - [Microsoft.DataBox](#microsoftdatabox)
> - [Microsoft.DataBoxEdge](#microsoftdataboxedge)
> - [Microsoft.Databricks](#microsoftdatabricks)
> - [Microsoft.DataCatalog](#microsoftdatacatalog)
> - [Microsoft.DataConnect](#microsoftdataconnect)
> - [Microsoft.DataExchange](#microsoftdataexchange)
> - [Microsoft.DataFactory](#microsoftdatafactory)
> - [Microsoft.DataLake](#microsoftdatalake)
> - [Microsoft.DataLakeAnalytics](#microsoftdatalakeanalytics)
> - [Microsoft.DataLakeStore](#microsoftdatalakestore)
> - [Microsoft.DataMigration](#microsoftdatamigration)
> - [Microsoft.DataProtection](#microsoftdataprotection)
> - [Microsoft.DataShare](#microsoftdatashare)
> - [Microsoft.DBforMariaDB](#microsoftdbformariadb)
> - [Microsoft.DBforMySQL](#microsoftdbformysql)
> - [Microsoft.DBforPostgreSQL](#microsoftdbforpostgresql)
> - [Microsoft.DeploymentManager](#microsoftdeploymentmanager)
> - [Microsoft.DesktopVirtualization](#microsoftdesktopvirtualization)
> - [Microsoft.Devices](#microsoftdevices)
> - [Microsoft.DevOps](#microsoftdevops)
> - [Microsoft.DevSpaces](#microsoftdevspaces)
> - [Microsoft.DevTestLab](#microsoftdevtestlab)
> - [Microsoft.DigitalTwins](#microsoftdigitaltwins)
> - [Microsoft.DocumentDB](#microsoftdocumentdb)
> - [Microsoft.DomainRegistration](#microsoftdomainregistration)
> - [Microsoft.EnterpriseKnowledgeGraph](#microsoftenterpriseknowledgegraph)
> - [Microsoft.EventGrid](#microsofteventgrid)
> - [Microsoft.EventHub](#microsofteventhub)
> - [Microsoft.Experimentation](#microsoftexperimentation)
> - [Microsoft.Falcon](#microsoftfalcon)
> - [Microsoft.Features](#microsoftfeatures)
> - [Microsoft.Genomics](#microsoftgenomics)
> - [Microsoft.GuestConfiguration](#microsoftguestconfiguration)
> - [Microsoft.HanaOnAzure](#microsofthanaonazure)
> - [Microsoft.HardwareSecurityModules](#microsofthardwaresecuritymodules)
> - [Microsoft.HDInsight](#microsofthdinsight)
> - [Microsoft.HealthcareApis](#microsofthealthcareapis)
> - [Microsoft.HybridCompute](#microsofthybridcompute)
> - [Microsoft.HybridData](#microsofthybriddata)
> - [Microsoft.HybridNetwork](#microsofthybridnetwork)
> - [Microsoft.Hydra](#microsofthydra)
> - [Microsoft.ImportExport](#microsoftimportexport)
> - [microsoft.insights](#microsoftinsights)
> - [Microsoft.IoTCentral](#microsoftiotcentral)
> - [Microsoft.IoTSpaces](#microsoftiotspaces)
> - [Microsoft.KeyVault](#microsoftkeyvault)
> - [Microsoft.Kubernetes](#microsoftkubernetes)
> - [Microsoft.KubernetesConfiguration](#microsoftkubernetesconfiguration)
> - [Microsoft.Kusto](#microsoftkusto)
> - [Microsoft.LabServices](#microsoftlabservices)
> - [Microsoft.LocationBasedServices](#microsoftlocationbasedservices)
> - [Microsoft.LocationServices](#microsoftlocationservices)
> - [Microsoft.Logic](#microsoftlogic)
> - [Microsoft.MachineLearning](#microsoftmachinelearning)
> - [Microsoft.MachineLearningCompute](#microsoftmachinelearningcompute)
> - [Microsoft.MachineLearningExperimentation](#microsoftmachinelearningexperimentation)
> - [Microsoft.MachineLearningModelManagement](#microsoftmachinelearningmodelmanagement)
> - [Microsoft.MachineLearningServices](#microsoftmachinelearningservices)
> - [Microsoft.Maintenance](#microsoftmaintenance)
> - [Microsoft.ManagedIdentity](#microsoftmanagedidentity)
> - [Microsoft.ManagedNetwork](#microsoftmanagednetwork)
> - [Microsoft.ManagedServices](#microsoftmanagedservices)
> - [Microsoft.Management](#microsoftmanagement)
> - [Microsoft.Maps](#microsoftmaps)
> - [Microsoft.Marketplace](#microsoftmarketplace)
> - [Microsoft.MarketplaceApps](#microsoftmarketplaceapps)
> - [Microsoft.MarketplaceOrdering](#microsoftmarketplaceordering)
> - [Microsoft.Media](#microsoftmedia)
> - [Microsoft.Microservices4Spring](#microsoftmicroservices4spring)
> - [Microsoft.Migrate](#microsoftmigrate)
> - [Microsoft.MixedReality](#microsoftmixedreality)
> - [Microsoft.NetApp](#microsoftnetapp)
> - [Microsoft.Network](#microsoftnetwork)
> - [Microsoft.NotificationHubs](#microsoftnotificationhubs)
> - [Microsoft.ObjectStore](#microsoftobjectstore)
> - [Microsoft.OffAzure](#microsoftoffazure)
> - [Microsoft.OperationalInsights](#microsoftoperationalinsights)
> - [Microsoft.OperationsManagement](#microsoftoperationsmanagement)
> - [Microsoft.Peering](#microsoftpeering)
> - [Microsoft.PolicyInsights](#microsoftpolicyinsights)
> - [Microsoft.Portal](#microsoftportal)
> - [Microsoft.PowerBI](#microsoftpowerbi)
> - [Microsoft.PowerBIDedicated](#microsoftpowerbidedicated)
> - [Microsoft.PowerPlatform](#microsoftpowerplatform)
> - [Microsoft.ProjectBabylon](#microsoftprojectbabylon)
> - [Microsoft.ProviderHub](#microsoftproviderhub)
> - [Microsoft.Quantum](#microsoftquantum)
> - [Microsoft.RecoveryServices](#microsoftrecoveryservices)
> - [Microsoft.RedHatOpenShift](#microsoftredhatopenshift)
> - [Microsoft.Relay](#microsoftrelay)
> - [Microsoft.ResourceGraph](#microsoftresourcegraph)
> - [Microsoft.ResourceHealth](#microsoftresourcehealth)
> - [Microsoft.Resources](#microsoftresources)
> - [Microsoft.SaaS](#microsoftsaas)
> - [Microsoft.Search](#microsoftsearch)
> - [Microsoft.Security](#microsoftsecurity)
> - [Microsoft.SecurityInsights](#microsoftsecurityinsights)
> - [Microsoft.SerialConsole](#microsoftserialconsole)
> - [Microsoft.ServerManagement](#microsoftservermanagement)
> - [Microsoft.ServiceBus](#microsoftservicebus)
> - [Microsoft.ServiceFabric](#microsoftservicefabric)
> - [Microsoft.ServiceFabricMesh](#microsoftservicefabricmesh)
> - [Microsoft.Services](#microsoftservices)
> - [Microsoft.SignalRService](#microsoftsignalrservice)
> - [Microsoft.SoftwarePlan](#microsoftsoftwareplan)
> - [Microsoft.Solutions](#microsoftsolutions)
> - [Microsoft.Sql](#microsoftsql)
> - [Microsoft.SqlVirtualMachine](#microsoftsqlvirtualmachine)
> - [Microsoft.Storage](#microsoftstorage)
> - [Microsoft.StorageCache](#microsoftstoragecache)
> - [Microsoft.StorageSync](#microsoftstoragesync)
> - [Microsoft.StorageSyncDev](#microsoftstoragesyncdev)
> - [Microsoft.StorageSyncInt](#microsoftstoragesyncint)
> - [Microsoft.StorSimple](#microsoftstorsimple)
> - [Microsoft.StreamAnalytics](#microsoftstreamanalytics)
> - [Microsoft.StreamAnalyticsExplorer](#microsoftstreamanalyticsexplorer)
> - [Microsoft.Subscription](#microsoftsubscription)
> - [microsoft.support](#microsoftsupport)
> - [Microsoft.Synapse](#microsoftsynapse)
> - [Microsoft.TimeSeriesInsights](#microsofttimeseriesinsights)
> - [Microsoft.Token](#microsofttoken)
> - [Microsoft.VirtualMachineImages](#microsoftvirtualmachineimages)
> - [microsoft.visualstudio](#microsoftvisualstudio)
> - [Microsoft.VMware](#microsoftvmware)
> - [Microsoft.VMwareCloudSimple](#microsoftvmwarecloudsimple)
> - [Microsoft.VnfManager](#microsoftvnfmanager)
> - [Microsoft.VSOnline](#microsoftvsonline)
> - [Microsoft.Web](#microsoftweb)
> - [Microsoft.WindowsESU](#microsoftwindowsesu)
> - [Microsoft.WindowsIoT](#microsoftwindowsiot)
> - [Microsoft.WorkloadBuilder](#microsoftworkloadbuilder)
> - [Microsoft.WorkloadMonitor](#microsoftworkloadmonitor)

## <a name="microsoftaad"></a>Microsoft.AAD

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | domainservices | × | × |
> | domainservices / oucontainer | × | × |
> | locations | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |

## <a name="microsoftaadiam"></a>microsoft.aadiam

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | diagnosticsettings | × | × |
> | diagnosticsettingscategories | × | × |
> | operations | × | × |
> | privatelinkforazuread | ○ | ○ |
> | tenants | ○ | ○ |

## <a name="microsoftaddons"></a>Microsoft.Addons

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operationresults | × | × |
> | operations | × | × |
> | supportproviders | × | × |

## <a name="microsoftadhybridhealthservice"></a>Microsoft.ADHybridHealthService

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | aadsupportcases | × | × |
> | addsservices | × | × |
> | agents | × | × |
> | anonymousapiusers | × | × |
> | configuration | × | × |
> | logs | × | × |
> | operations | × | × |
> | reports | × | × |
> | servicehealthmetrics | × | × |
> | services | × | × |

## <a name="microsoftadvisor"></a>Microsoft.Advisor

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | configuration | × | × |
> | generaterecommendations | × | × |
> | metadata | × | × |
> | operations | × | × |
> | recommendations | × | × |
> | suppressions | × | × |

## <a name="microsoftalertsmanagement"></a>Microsoft.AlertsManagement

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | actionrules | ○ | ○ |
> | alerts | × | × |
> | alertslist | × | × |
> | alertsmetadata | × | × |
> | alertssummary | × | × |
> | alertssummarylist | × | × |
> | operations | × | × |
> | smartdetectoralertrules | ○ | ○ |
> | smartgroups | × | × |

## <a name="microsoftanalysisservices"></a>Microsoft.AnalysisServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | servers | ○ | ○ |

## <a name="microsoftapimanagement"></a>Microsoft.ApiManagement

> [!IMPORTANT]
> 従量課金 SKU に設定されている API Management サービスは移動できません。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checkfeedbackrequired | × | × |
> | checknameavailability | × | × |
> | checkservicenameavailability | × | × |
> | operations | × | × |
> | reportfeedback | × | × |
> | サービス (service) | ○ | ○ |
> | validateservicename | × | × |

## <a name="microsoftappconfiguration"></a>Microsoft.AppConfiguration

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | configurationstores | ○ | ○ |
> | configurationstores / eventgridfilters | × | × |
> | locations | × | × |
> | locations / operationsstatus | × | × |
> | operations | × | × |

## <a name="microsoftappplatform"></a>Microsoft.AppPlatform

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / operationstatus | × | × |
> | operations | × | × |
> | spring | ○ | ○ |
> | spring / apps | × | × |
> | spring / apps / deployments | × | × |

## <a name="microsoftappservice"></a>Microsoft.AppService

> [!IMPORTANT]
> [App Service move guidance (App Service の移動のガイダンス)](./move-limitations/app-service-move-limitations.md) に関する記事をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | apiapps | × | × |
> | appidentities | × | × |
> | gateways | × | × |

## <a name="microsoftattestation"></a>Microsoft.Attestation

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | attestationproviders | ○ | ○ |
> | operations | × | × |

## <a name="microsoftauthorization"></a>Microsoft.Authorization

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checkaccess | × | × |
> | classicadministrators | × | × |
> | dataaliases | × | × |
> | denyassignments | × | × |
> | elevateaccess | × | × |
> | findorphanroleassignments | × | × |
> | locks | × | × |
> | operations | × | × |
> | operationstatus | × | × |
> | 権限 | × | × |
> | policyassignments | × | × |
> | policydefinitions | × | × |
> | policysetdefinitions | × | × |
> | privatelinkassociations | × | × |
> | provideroperations | × | × |
> | resourcemanagementprivatelinks | × | × |
> | roleassignments | × | × |
> | roleassignmentsusagemetrics | × | × |
> | roledefinitions | × | × |

## <a name="microsoftautomation"></a>Microsoft.Automation

> [!IMPORTANT]
> Runbook は Automation アカウントと同じリソース グループに存在する必要があります。
>
> 詳しくは、「[Azure Automation アカウントを別のサブスクリプションに移動する](../../automation/how-to/move-account.md?toc=/azure/azure-resource-manager/toc.json)」をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | automationaccounts | ○ | ○ |
> | automationaccounts/configurations | ○ | ○ |
> | automationaccounts / jobs | × | × |
> | automationaccounts / privateendpointconnectionproxies | × | × |
> | automationaccounts / privateendpointconnections | × | × |
> | automationaccounts / privatelinkresources | × | × |
> | automationaccounts/runbooks | ○ | ○ |
> | automationaccounts / softwareupdateconfigurations | × | × |
> | automationaccounts / webhooks | × | × |
> | operations | × | × |

## <a name="microsoftavs"></a>Microsoft.AVS

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / checkquotaavailability | × | × |
> | locations / checktrialavailability | × | × |
> | operations | × | × |
> | privateclouds | ○ | ○ |
> | privateclouds / clusters | × | × |

## <a name="microsoftazureactivedirectory"></a>Microsoft.AzureActiveDirectory

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | b2cdirectories | ○ | ○ |
> | b2ctenants | × | × |
> | checknameavailability | × | × |
> | operations | × | × |

## <a name="microsoftazuredata"></a>Microsoft.AzureData

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | datacontrollers | × | × |
> | hybriddatamanagers | × | × |
> | operations | × | × |
> | postgresinstances | × | × |
> | sqlinstances | × | × |
> | sqlmanagedinstances | × | × |
> | sqlserverinstances | × | × |
> | sqlserverregistrations | ○ | ○ |
> | sqlserverregistrations / sqlservers | × | × |

## <a name="microsoftazurestack"></a>Microsoft.AzureStack

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | cloudmanifestfiles | × | × |
> | operations | × | × |
> | registrations | ○ | ○ |
> | registrations / customersubscriptions | × | × |
> | registrations / products | × | × |

## <a name="microsoftazurestackhci"></a>Microsoft.AzureStackHCI

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | clusters | × | × |
> | operations | × | × |

## <a name="microsoftbatch"></a>Microsoft.Batch

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | batchaccounts | ○ | ○ |
> | locations | × | × |
> | locations / accountoperationresults | × | × |
> | locations / checknameavailability | × | × |
> | locations / quotas | × | × |
> | operations | × | × |

## <a name="microsoftbilling"></a>Microsoft.Billing

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | billingaccounts | × | × |
> | billingaccounts / agreements | × | × |
> | billingaccounts / billingpermissions | × | × |
> | billingaccounts / billingprofiles | × | × |
> | billingaccounts / billingprofiles / availablebalance | × | × |
> | billingaccounts / billingprofiles / billingpermissions | × | × |
> | billingaccounts / billingprofiles / billingroleassignments | × | × |
> | billingaccounts / billingprofiles / billingroledefinitions | × | × |
> | billingaccounts / billingprofiles / billingsubscriptions | × | × |
> | billingaccounts / billingprofiles / createbillingroleassignment | × | × |
> | billingaccounts / billingprofiles / customers | × | × |
> | billingaccounts / billingprofiles / instructions | × | × |
> | billingaccounts / billingprofiles / invoices | × | × |
> | billingaccounts / billingprofiles / invoices / pricesheet | × | × |
> | billingaccounts / billingprofiles / invoices / transactions | × | × |
> | billingaccounts / billingprofiles / invoicesections | × | × |
> | billingaccounts / billingprofiles / invoicesections / billingpermissions | × | × |
> | billingaccounts / billingprofiles / invoicesections / billingroleassignments | × | × |
> | billingaccounts / billingprofiles / invoicesections / billingroledefinitions | × | × |
> | billingaccounts / billingprofiles / invoicesections / billingsubscriptions | × | × |
> | billingaccounts / billingprofiles / invoicesections / createbillingroleassignment | × | × |
> | billingaccounts / billingprofiles / invoicesections / initiatetransfer | × | × |
> | billingaccounts / billingprofiles / invoicesections / products | × | × |
> | billingaccounts / billingprofiles / invoicesections / products / transfer | × | × |
> | billingaccounts / billingprofiles / invoicesections / products / updateautorenew | × | × |
> | billingaccounts / billingprofiles / invoicesections / transactions | × | × |
> | billingaccounts / billingprofiles / invoicesections / transfers | × | × |
> | billingaccounts / billingprofiles / patchoperations | × | × |
> | billingaccounts / billingprofiles / paymentmethods | × | × |
> | billingaccounts / billingprofiles / policies | × | × |
> | billingaccounts / billingprofiles / pricesheet | × | × |
> | billingaccounts / billingprofiles / pricesheetdownloadoperations | × | × |
> | billingaccounts / billingprofiles / products | × | × |
> | billingaccounts / billingprofiles / transactions | × | × |
> | billingaccounts / billingroleassignments | × | × |
> | billingaccounts / billingroledefinitions | × | × |
> | billingaccounts / billingsubscriptions | × | × |
> | billingaccounts / billingsubscriptions / invoices | × | × |
> | billingaccounts / createbillingroleassignment | × | × |
> | billingaccounts / createinvoicesectionoperations | × | × |
> | billingaccounts / customers | × | × |
> | billingaccounts / customers / billingpermissions | × | × |
> | billingaccounts / customers / billingsubscriptions | × | × |
> | billingaccounts / customers / initiatetransfer | × | × |
> | billingaccounts / customers / policies | × | × |
> | billingaccounts / customers / products | × | × |
> | billingaccounts / customers / transactions | × | × |
> | billingaccounts / customers / transfers | × | × |
> | billingaccounts / departments | × | × |
> | billingaccounts / enrollmentaccounts | × | × |
> | billingaccounts / invoices | × | × |
> | billingaccounts / invoicesections | × | × |
> | billingaccounts / invoicesections / billingsubscriptionmoveoperations | × | × |
> | billingaccounts / invoicesections / billingsubscriptions | × | × |
> | billingaccounts / invoicesections / billingsubscriptions / transfer | × | × |
> | billingaccounts / invoicesections / elevate | × | × |
> | billingaccounts / invoicesections / initiatetransfer | × | × |
> | billingaccounts / invoicesections / patchoperations | × | × |
> | billingaccounts / invoicesections / productmoveoperations | × | × |
> | billingaccounts / invoicesections / products | × | × |
> | billingaccounts / invoicesections / products / transfer | × | × |
> | billingaccounts / invoicesections / products / updateautorenew | × | × |
> | billingaccounts / invoicesections / producttransfersresults | × | × |
> | billingaccounts / invoicesections / transactions | × | × |
> | billingaccounts / invoicesections / transfers | × | × |
> | billingaccounts / lineofcredit | × | × |
> | billingaccounts / listinvoicesectionswithcreatesubscriptionpermission | × | × |
> | billingaccounts / operationresults | × | × |
> | billingaccounts / patchoperations | × | × |
> | billingaccounts / paymentmethods | × | × |
> | billingaccounts / products | × | × |
> | billingaccounts / transactions | × | × |
> | billingperiods | × | × |
> | billingpermissions | × | × |
> | billingproperty | × | × |
> | billingroleassignments | × | × |
> | billingroledefinitions | × | × |
> | createbillingroleassignment | × | × |
> | departments | × | × |
> | enrollmentaccounts | × | × |
> | invoices | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | operationstatus | × | × |
> | transfers | × | × |
> | transfers / accepttransfer | × | × |
> | transfers / declinetransfer | × | × |
> | transfers / operationstatus | × | × |
> | transfers / validatetransfer | × | × |
> | validateaddress | × | × |

## <a name="microsoftbingmaps"></a>Microsoft.BingMaps

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | listcommunicationpreference | × | × |
> | mapapis | × | × |
> | operations | × | × |
> | updatecommunicationpreference | × | × |

## <a name="microsoftbiztalkservices"></a>Microsoft.BizTalkServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | biztalk | × | × |

## <a name="microsoftblockchain"></a>Microsoft.Blockchain

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | blockchainmembers | × | × |
> | cordamembers | × | × |
> | locations | × | × |
> | locations / blockchainmemberoperationresults | × | × |
> | locations / checknameavailability | × | × |
> | locations / listconsortiums | × | × |
> | locations / watcheroperationresults | × | × |
> | operations | × | × |
> | watchers | × | × |

## <a name="microsoftblockchaintokens"></a>Microsoft.BlockchainTokens

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |
> | tokenservices | × | × |

## <a name="microsoftblueprint"></a>Microsoft.Blueprint

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | blueprintassignments | × | × |
> | blueprintassignments / assignmentoperations | × | × |
> | blueprintassignments / operations | × | × |
> | blueprints | × | × |
> | blueprints / artifacts | × | × |
> | blueprints / versions | × | × |
> | blueprints / versions / artifacts | × | × |
> | operations | × | × |

## <a name="microsoftbotservice"></a>Microsoft.BotService

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | botservices | ○ | ○ |
> | botservices / channels | × | × |
> | botservices / connections | × | × |
> | checknameavailability | × | × |
> | listauthserviceproviders | × | × |
> | operations | × | × |

## <a name="microsoftcache"></a>Microsoft.Cache

> [!IMPORTANT]
> 仮想ネットワークを使用して Azure Cache for Redis インスタンスが構成されている場合、インスタンスを別のサブスクリプションに移動させることはできません。 「[ネットワーク リソースの移動ガイダンス](./move-limitations/networking-move-limitations.md)」を参照してください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / operationresults | × | × |
> | locations / operationsstatus | × | × |
> | operations | × | × |
> | redis | ○ | ○ |
> | redis / eventgridfilters | × | × |
> | redis / privatelinkresources | × | × |
> | redisenterprise | × | × |

## <a name="microsoftcapacity"></a>Microsoft.Capacity

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | appliedreservations | × | × |
> | calculateexchange | × | × |
> | calculateprice | × | × |
> | calculatepurchaseprice | × | × |
> | catalogs | × | × |
> | checkoffers | × | × |
> | checkpurchasestatus | × | × |
> | checkscopes | × | × |
> | commercialreservationorders | × | × |
> | exchange | × | × |
> | listbenefits | × | × |
> | operations | × | × |
> | placepurchaseorder | × | × |
> | reservationorders | × | × |
> | reservationorders / availablescopes | × | × |
> | reservationorders / calculaterefund | × | × |
> | reservationorders / merge | × | × |
> | reservationorders / reservations | × | × |
> | reservationorders / reservations / availablescopes | × | × |
> | reservationorders / reservations / revisions | × | × |
> | reservationorders / return | × | × |
> | reservationorders / split | × | × |
> | reservationorders / swap | × | × |
> | reservations | × | × |
> | resources | × | × |
> | validatereservationorder | × | × |

## <a name="microsoftcdn"></a>Microsoft.Cdn

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | cdnwebapplicationfirewallmanagedrulesets | × | × |
> | cdnwebapplicationfirewallpolicies | ○ | ○ |
> | checknameavailability | × | × |
> | checkresourceusage | × | × |
> | edgenodes | × | × |
> | operationresults | × | × |
> | operationresults / profileresults | × | × |
> | operationresults / profileresults / endpointresults | × | × |
> | operationresults / profileresults / endpointresults / customdomainresults | × | × |
> | operationresults / profileresults / endpointresults / origingroupresults | × | × |
> | operationresults / profileresults / endpointresults / originresults | × | × |
> | operations | × | × |
> | profiles | ○ | ○ |
> | profiles/endpoints | ○ | ○ |
> | profiles / endpoints / customdomains | × | × |
> | profiles / endpoints / origingroups | × | × |
> | profiles / endpoints / origins | × | × |
> | validateprobe | × | × |

## <a name="microsoftcertificateregistration"></a>Microsoft.CertificateRegistration

> [!IMPORTANT]
> [App Service move guidance (App Service の移動のガイダンス)](./move-limitations/app-service-move-limitations.md) に関する記事をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | certificateorders | ○ | ○ |
> | certificateorders / certificates | × | × |
> | operations | × | × |
> | validatecertificateregistrationinformation | × | × |

## <a name="microsoftchangeanalysis"></a>Microsoft.ChangeAnalysis

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |

## <a name="microsoftclassiccompute"></a>Microsoft.ClassicCompute

> [!IMPORTANT]
> [Classic deployment move guidance (クラシック デプロイの移動のガイダンス)](./move-limitations/classic-model-move-limitations.md) に関する記事をご覧ください。 クラシック デプロイのリソースは、そのシナリオに固有の操作を使用して、サブスクリプション間で移動できます。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | capabilities | × | × |
> | checkdomainnameavailability | × | × |
> | domainnames | ○ | × |
> | domainnames / capabilities | × | × |
> | domainnames / internalloadbalancers | × | × |
> | domainnames / servicecertificates | × | × |
> | domainnames / slots | × | × |
> | domainnames / slots / roles | × | × |
> | domainnames / slots / roles / metricdefinitions | × | × |
> | domainnames / slots / roles / metrics | × | × |
> | movesubscriptionresources | × | × |
> | operatingsystemfamilies | × | × |
> | operatingsystems | × | × |
> | operations | × | × |
> | operationstatuses | × | × |
> | quotas | × | × |
> | resourcetypes | × | × |
> | validatesubscriptionmoveavailability | × | × |
> | virtualmachines | ○ | × |
> | virtualmachines / diagnosticsettings | × | × |
> | virtualmachines / metricdefinitions | × | × |
> | virtualmachines / metrics | × | × |

## <a name="microsoftclassicinfrastructuremigrate"></a>Microsoft.ClassicInfrastructureMigrate

> [!IMPORTANT]
> [Classic deployment move guidance (クラシック デプロイの移動のガイダンス)](./move-limitations/classic-model-move-limitations.md) に関する記事をご覧ください。 クラシック デプロイのリソースは、そのシナリオに固有の操作を使用して、サブスクリプション間で移動できます。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | classicinfrastructureresources | × | × |

## <a name="microsoftclassicnetwork"></a>Microsoft.ClassicNetwork

> [!IMPORTANT]
> [Classic deployment move guidance (クラシック デプロイの移動のガイダンス)](./move-limitations/classic-model-move-limitations.md) に関する記事をご覧ください。 クラシック デプロイのリソースは、そのシナリオに固有の操作を使用して、サブスクリプション間で移動できます。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | capabilities | × | × |
> | expressroutecrossconnections | × | × |
> | expressroutecrossconnections / peerings | × | × |
> | gatewaysupporteddevices | × | × |
> | networksecuritygroups | × | × |
> | operations | × | × |
> | quotas | × | × |
> | reservedips | × | × |
> | virtualnetworks | × | × |
> | virtualnetworks / remotevirtualnetworkpeeringproxies | × | × |
> | virtualnetworks / virtualnetworkpeerings | × | × |

## <a name="microsoftclassicstorage"></a>Microsoft.ClassicStorage

> [!IMPORTANT]
> [Classic deployment move guidance (クラシック デプロイの移動のガイダンス)](./move-limitations/classic-model-move-limitations.md) に関する記事をご覧ください。 クラシック デプロイのリソースは、そのシナリオに固有の操作を使用して、サブスクリプション間で移動できます。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | capabilities | × | × |
> | checkstorageaccountavailability | × | × |
> | disks | × | × |
> | images | × | × |
> | operations | × | × |
> | osimages | × | × |
> | osplatformimages | × | × |
> | publicimages | × | × |
> | quotas | × | × |
> | storageaccounts | ○ | × |
> | storageaccounts / blobservices | × | × |
> | storageaccounts / fileservices | × | × |
> | storageaccounts / metricdefinitions | × | × |
> | storageaccounts / metrics | × | × |
> | storageaccounts / queueservices | × | × |
> | storageaccounts / services | × | × |
> | storageaccounts / services / diagnosticsettings | × | × |
> | storageaccounts / services / metricdefinitions | × | × |
> | storageaccounts / services / metrics | × | × |
> | storageaccounts / tableservices | × | × |
> | storageaccounts / vmimages | × | × |
> | vmimages | × | × |

## <a name="microsoftclassicsubscription"></a>Microsoft.ClassicSubscription

> [!IMPORTANT]
> [Classic deployment move guidance (クラシック デプロイの移動のガイダンス)](./move-limitations/classic-model-move-limitations.md) に関する記事をご覧ください。 クラシック デプロイのリソースは、そのシナリオに固有の操作を使用して、サブスクリプション間で移動できます。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |

## <a name="microsoftcognitiveservices"></a>Microsoft.CognitiveServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | ○ | ○ |
> | checkdomainavailability | × | × |
> | locations | × | × |
> | locations / checkskuavailability | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |

## <a name="microsoftcommerce"></a>Microsoft.Commerce

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |
> | ratecard | × | × |
> | usageaggregates | × | × |

## <a name="microsoftcompute"></a>Microsoft.Compute

> [!IMPORTANT]
> [Virtual Machines move guidance (仮想マシンの移動のガイダンス)](./move-limitations/virtual-machines-move-limitations.md) に関する記事をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | availabilitysets | ○ | ○ |
> | diskaccesses | × | × |
> | diskencryptionsets | × | × |
> | disks | ○ | ○ |
> | galleries | × | × |
> | galleries/images | × | × |
> | galleries/images/versions | × | × |
> | hostgroups | × | × |
> | hostgroups/hosts | × | × |
> | images | ○ | ○ |
> | locations | × | × |
> | locations / artifactpublishers | × | × |
> | locations / capsoperations | × | × |
> | locations / diskoperations | × | × |
> | locations / loganalytics | × | × |
> | locations / operations | × | × |
> | locations / publishers | × | × |
> | locations / runcommands | × | × |
> | locations / usages | × | × |
> | locations / virtualmachines | × | × |
> | locations / vmsizes | × | × |
> | locations / vsmoperations | × | × |
> | operations | × | × |
> | proximityplacementgroups | ○ | ○ |
> | restorepointcollections | × | × |
> | restorepointcollections / restorepoints | × | × |
> | sharedvmextensions | × | × |
> | sharedvmimages | × | × |
> | sharedvmimages/versions | × | × |
> | スナップショット | ○ | ○ |
> | sshpublickeys | × | × |
> | virtualmachines | ○ | ○ |
> | virtualmachines/extensions | ○ | ○ |
> | virtualmachines / metricdefinitions | × | × |
> | virtualmachines / runcommands | × | × |
> | virtualmachinescalesets | ○ | ○ |
> | virtualmachinescalesets / extensions | × | × |
> | virtualmachinescalesets / networkinterfaces | × | × |
> | virtualmachinescalesets / publicipaddresses | × | × |
> | virtualmachinescalesets / virtualmachines | × | × |
> | virtualmachinescalesets / virtualmachines / networkinterfaces | × | × |

## <a name="microsoftconsumption"></a>Microsoft.Consumption

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | aggregatedcost | × | × |
> | balances | × | × |
> | budgets | × | × |
> | charges | × | × |
> | costtags | × | × |
> | credits | × | × |
> | events | × | × |
> | forecasts | × | × |
> | lots | × | × |
> | marketplaces | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | operationstatus | × | × |
> | pricesheets | × | × |
> | products | × | × |
> | reservationdetails | × | × |
> | reservationrecommendationdetails | × | × |
> | reservationrecommendations | × | × |
> | reservationsummaries | × | × |
> | reservationtransactions | × | × |
> | tags | × | × |
> | tenants | × | × |
> | terms | × | × |
> | usagedetails | × | × |

## <a name="microsoftcontainerinstance"></a>Microsoft.ContainerInstance

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | containergroups | × | × |
> | locations | × | × |
> | locations / cachedimages | × | × |
> | locations / capabilities | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / operations | × | × |
> | locations / usages | × | × |
> | operations | × | × |
> | serviceassociationlinks | × | × |

## <a name="microsoftcontainerregistry"></a>Microsoft.ContainerRegistry

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / authorize | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / operationresults | × | × |
> | locations / setupauth | × | × |
> | operations | × | × |
> | registries | ○ | ○ |
> | registries / agentpools | ○ | ○ |
> | registries / agentpools / listqueuestatus | × | × |
> | registries / builds | × | × |
> | registries / builds / cancel | × | × |
> | registries / builds / getloglink | × | × |
> | registries/buildtasks | ○ | ○ |
> | registries / buildtasks / listsourcerepositoryproperties | × | × |
> | registries / buildtasks / steps | × | × |
> | registries / buildtasks / steps / listbuildarguments | × | × |
> | registries / eventgridfilters | × | × |
> | registries / exportpipelines | × | × |
> | registries / generatecredentials | × | × |
> | registries / getbuildsourceuploadurl | × | × |
> | registries / getcredentials | × | × |
> | registries / importimage | × | × |
> | registries / importpipelines | × | × |
> | registries / listbuildsourceuploadurl | × | × |
> | registries / listcredentials | × | × |
> | registries / listpolicies | × | × |
> | registries / listusages | × | × |
> | registries / pipelineruns | × | × |
> | registries / privateendpointconnectionproxies | × | × |
> | registries / privateendpointconnectionproxies / validate | × | × |
> | registries / privateendpointconnections | × | × |
> | registries / privatelinkresources | × | × |
> | registries / queuebuild | × | × |
> | registries / regeneratecredential | × | × |
> | registries / regeneratecredentials | × | × |
> | registries/replications | ○ | ○ |
> | registries / runs | × | × |
> | registries / runs / cancel | × | × |
> | registries / runs / listlogsasurl | × | × |
> | registries / schedulerun | × | × |
> | registries / scopemaps | × | × |
> | registries/taskruns | × | × |
> | registries / taskruns / listdetails | × | × |
> | registries/tasks | ○ | ○ |
> | registries / tasks / listdetails | × | × |
> | registries / tokens | × | × |
> | registries / updatepolicies | × | × |
> | registries/webhooks | ○ | ○ |
> | registries / webhooks / getcallbackconfig | × | × |
> | registries / webhooks / listevents | × | × |
> | registries / webhooks / ping | × | × |

## <a name="microsoftcontainerservice"></a>Microsoft.ContainerService

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | containerservices | × | × |
> | locations | × | × |
> | locations / openshiftclusters | × | × |
> | locations / operationresults | × | × |
> | locations / operations | × | × |
> | locations / orchestrators | × | × |
> | managedclusters | × | × |
> | openshiftmanagedclusters | × | × |
> | operations | × | × |

## <a name="microsoftcontentmoderator"></a>Microsoft.ContentModerator

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applications | × | × |

## <a name="microsoftcortanaanalytics"></a>Microsoft.CortanaAnalytics

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |

## <a name="microsoftcostmanagement"></a>Microsoft.CostManagement

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | alerts | × | × |
> | billingaccounts | × | × |
> | budgets | × | × |
> | cloudconnectors | × | × |
> | connectors | ○ | ○ |
> | departments | × | × |
> | dimensions | × | × |
> | enrollmentaccounts | × | × |
> | exports | × | × |
> | externalbillingaccounts | × | × |
> | externalbillingaccounts / alerts | × | × |
> | externalbillingaccounts / dimensions | × | × |
> | externalbillingaccounts / forecast | × | × |
> | externalbillingaccounts / query | × | × |
> | externalsubscriptions | × | × |
> | externalsubscriptions / alerts | × | × |
> | externalsubscriptions / dimensions | × | × |
> | externalsubscriptions / forecast | × | × |
> | externalsubscriptions / query | × | × |
> | forecast | × | × |
> | operations | × | × |
> | query | × | × |
> | registrations | × | × |
> | reportconfigs | × | × |
> | reports | × | × |
> | settings | × | × |
> | showbackrules | × | × |
> | views | × | × |

## <a name="microsoftcostmanagementexports"></a>Microsoft.CostManagementExports

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |

## <a name="microsoftcustomerinsights"></a>Microsoft.CustomerInsights

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | hubs | × | × |

## <a name="microsoftcustomerlockbox"></a>Microsoft.CustomerLockbox

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |
> | requests | × | × |

## <a name="microsoftcustomproviders"></a>Microsoft.CustomProviders

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | associations | × | × |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | resourceproviders | ○ | ○ |

## <a name="microsoftdatabox"></a>Microsoft.DataBox

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | jobs | × | × |
> | locations | × | × |
> | locations / availableskus | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / regionconfiguration | × | × |
> | locations / validateaddress | × | × |
> | locations / validateinputs | × | × |
> | operations | × | × |

## <a name="microsoftdataboxedge"></a>Microsoft.DataBoxEdge

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | availableskus | × | × |
> | databoxedgedevices | ○ | ○ |
> | databoxedgedevices / checknameavailability | × | × |
> | operations | × | × |

## <a name="microsoftdatabricks"></a>Microsoft.Databricks

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / getnetworkpolicies | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | workspaces | × | × |
> | workspaces / dbworkspaces | × | × |
> | workspaces / virtualnetworkpeerings | × | × |

## <a name="microsoftdatacatalog"></a>Microsoft.DataCatalog

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | catalogs | ○ | ○ |
> | checknameavailability | × | × |
> | datacatalogs | × | × |
> | locations | × | × |
> | locations / jobs | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |

## <a name="microsoftdataconnect"></a>Microsoft.DataConnect

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | connectionmanagers | × | × |

## <a name="microsoftdataexchange"></a>Microsoft.DataExchange

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | packages | × | × |
> | plans | × | × |

## <a name="microsoftdatafactory"></a>Microsoft.DataFactory

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checkazuredatafactorynameavailability | × | × |
> | checkdatafactorynameavailability | × | × |
> | datafactories | ○ | ○ |
> | datafactories / diagnosticsettings | × | × |
> | datafactories / metricdefinitions | × | × |
> | datafactoryschema | × | × |
> | factories | ○ | ○ |
> | factories / integrationruntimes | × | × |
> | locations | × | × |
> | locations / configurefactoryrepo | × | × |
> | locations / getfeaturevalue | × | × |
> | operations | × | × |

## <a name="microsoftdatalake"></a>Microsoft.DataLake

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | datalakeaccounts | × | × |

## <a name="microsoftdatalakeanalytics"></a>Microsoft.DataLakeAnalytics

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | ○ | ○ |
> | accounts / datalakestoreaccounts | × | × |
> | accounts / storageaccounts | × | × |
> | accounts / storageaccounts / containers | × | × |
> | accounts / storageaccounts / containers / listsastokens | × | × |
> | locations | × | × |
> | locations / capability | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / usages | × | × |
> | operations | × | × |

## <a name="microsoftdatalakestore"></a>Microsoft.DataLakeStore

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | ○ | ○ |
> | accounts / eventgridfilters | × | × |
> | accounts / firewallrules | × | × |
> | locations | × | × |
> | locations / capability | × | × |
> | locations / checknameavailability | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / operationresults | × | × |
> | locations / usages | × | × |
> | operations | × | × |

## <a name="microsoftdatamigration"></a>Microsoft.DataMigration

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | services | × | × |
> | services/projects | × | × |
> | slots | × | × |

## <a name="microsoftdataprotection"></a>Microsoft.DataProtection

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | backupvaults | × | × |
> | locations | × | × |
> | operations | × | × |

## <a name="microsoftdatashare"></a>Microsoft.DataShare

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | ○ | ○ |
> | accounts / shares | × | × |
> | accounts / shares / datasets | × | × |
> | accounts / shares / invitations | × | × |
> | accounts / shares / providersharesubscriptions | × | × |
> | accounts / shares / synchronizationsettings | × | × |
> | accounts / sharesubscriptions | × | × |
> | accounts / sharesubscriptions / consumersourcedatasets | × | × |
> | accounts / sharesubscriptions / datasetmappings | × | × |
> | accounts / sharesubscriptions / triggers | × | × |
> | listinvitations | × | × |
> | locations | × | × |
> | locations / consumerinvitations | × | × |
> | locations / operationresults | × | × |
> | locations / rejectinvitation | × | × |
> | operations | × | × |

## <a name="microsoftdbformariadb"></a>Microsoft.DBforMariaDB

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / azureasyncoperation | × | × |
> | locations / operationresults | × | × |
> | locations / performancetiers | × | × |
> | locations / privateendpointconnectionazureasyncoperation | × | × |
> | locations / privateendpointconnectionoperationresults | × | × |
> | locations / privateendpointconnectionproxyazureasyncoperation | × | × |
> | locations / privateendpointconnectionproxyoperationresults | × | × |
> | locations / recommendedactionsessionsazureasyncoperation | × | × |
> | locations / recommendedactionsessionsoperationresults | × | × |
> | locations / securityalertpoliciesazureasyncoperation | × | × |
> | locations / securityalertpoliciesoperationresults | × | × |
> | locations / serverkeyazureasyncoperation | × | × |
> | locations / serverkeyoperationresults | × | × |
> | operations | × | × |
> | servers | ○ | ○ |
> | servers / advisors | × | × |
> | servers / privateendpointconnectionproxies | × | × |
> | servers / privateendpointconnections | × | × |
> | servers / privatelinkresources | × | × |
> | servers / querytexts | × | × |
> | servers / recoverableservers | × | × |
> | servers / topquerystatistics | × | × |
> | servers / virtualnetworkrules | × | × |
> | servers / waitstatistics | × | × |

## <a name="microsoftdbformysql"></a>Microsoft.DBforMySQL

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / administratorazureasyncoperation | × | × |
> | locations / administratoroperationresults | × | × |
> | locations / azureasyncoperation | × | × |
> | locations / operationresults | × | × |
> | locations / performancetiers | × | × |
> | locations / privateendpointconnectionazureasyncoperation | × | × |
> | locations / privateendpointconnectionoperationresults | × | × |
> | locations / privateendpointconnectionproxyazureasyncoperation | × | × |
> | locations / privateendpointconnectionproxyoperationresults | × | × |
> | locations / recommendedactionsessionsazureasyncoperation | × | × |
> | locations / recommendedactionsessionsoperationresults | × | × |
> | locations / securityalertpoliciesazureasyncoperation | × | × |
> | locations / securityalertpoliciesoperationresults | × | × |
> | locations / serverkeyazureasyncoperation | × | × |
> | locations / serverkeyoperationresults | × | × |
> | operations | × | × |
> | servers | ○ | ○ |
> | servers / advisors | × | × |
> | servers / keys | × | × |
> | servers / privateendpointconnectionproxies | × | × |
> | servers / privateendpointconnections | × | × |
> | servers / privatelinkresources | × | × |
> | servers / querytexts | × | × |
> | servers / recoverableservers | × | × |
> | servers / topquerystatistics | × | × |
> | servers / virtualnetworkrules | × | × |
> | servers / waitstatistics | × | × |

## <a name="microsoftdbforpostgresql"></a>Microsoft.DBforPostgreSQL

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / administratorazureasyncoperation | × | × |
> | locations / administratoroperationresults | × | × |
> | locations / azureasyncoperation | × | × |
> | locations / operationresults | × | × |
> | locations / performancetiers | × | × |
> | locations / privateendpointconnectionazureasyncoperation | × | × |
> | locations / privateendpointconnectionoperationresults | × | × |
> | locations / privateendpointconnectionproxyazureasyncoperation | × | × |
> | locations / privateendpointconnectionproxyoperationresults | × | × |
> | locations / recommendedactionsessionsazureasyncoperation | × | × |
> | locations / recommendedactionsessionsoperationresults | × | × |
> | locations / securityalertpoliciesazureasyncoperation | × | × |
> | locations / securityalertpoliciesoperationresults | × | × |
> | locations / serverkeyazureasyncoperation | × | × |
> | locations / serverkeyoperationresults | × | × |
> | operations | × | × |
> | servergroups | × | × |
> | servers | ○ | ○ |
> | servers / advisors | × | × |
> | servers / keys | × | × |
> | servers / privateendpointconnectionproxies | × | × |
> | servers / privateendpointconnections | × | × |
> | servers / privatelinkresources | × | × |
> | servers / querytexts | × | × |
> | servers / recoverableservers | × | × |
> | servers / topquerystatistics | × | × |
> | servers / virtualnetworkrules | × | × |
> | servers / waitstatistics | × | × |
> | serversv2 | ○ | ○ |
> | singleservers | ○ | ○ |

## <a name="microsoftdeploymentmanager"></a>Microsoft.DeploymentManager

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | artifactsources | ○ | ○ |
> | operationresults | × | × |
> | operations | × | × |
> | rollouts | ○ | ○ |
> | servicetopologies | ○ | ○ |
> | servicetopologies/services | ○ | ○ |
> | servicetopologies/services/serviceunits | ○ | ○ |
> | steps | ○ | ○ |

## <a name="microsoftdesktopvirtualization"></a>Microsoft.DesktopVirtualization

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applicationgroups | ○ | ○ |
> | applicationgroups / applications | × | × |
> | applicationgroups / desktops | × | × |
> | applicationgroups / startmenuitems | × | × |
> | hostpools | ○ | ○ |
> | hostpools / sessionhosts | × | × |
> | hostpools / sessionhosts / usersessions | × | × |
> | hostpools / usersessions | × | × |
> | operations | × | × |
> | workspaces | ○ | ○ |

## <a name="microsoftdevices"></a>Microsoft.Devices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | checkprovisioningservicenameavailability | × | × |
> | elasticpools | × | × |
> | elasticpools/iothubtenants | × | × |
> | iothubs | ○ | ○ |
> | iothubs / eventgridfilters | × | × |
> | iothubs / securitysettings | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | provisioningservices | ○ | ○ |
> | usages | × | × |

## <a name="microsoftdevops"></a>Microsoft.DevOps

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | pipelines | ○ | ○ |

## <a name="microsoftdevspaces"></a>Microsoft.DevSpaces

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | controllers | ○ | ○ |
> | controllers / listconnectiondetails | × | × |
> | locations | × | × |
> | locations / checkcontainerhostmapping | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |

## <a name="microsoftdevtestlab"></a>Microsoft.DevTestLab

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | labcenters | × | × |
> | labs | ○ | × |
> | labs/environments | ○ | ○ |
> | labs/servicerunners | ○ | ○ |
> | labs/virtualmachines | ○ | × |
> | locations | × | × |
> | locations / operations | × | × |
> | operations | × | × |
> | schedules | ○ | ○ |

## <a name="microsoftdigitaltwins"></a>Microsoft.DigitalTwins

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | digitaltwinsinstances | × | × |
> | digitaltwinsinstances / operationresults | × | × |
> | locations | × | × |
> | operations | × | × |

## <a name="microsoftdocumentdb"></a>Microsoft.DocumentDB

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | databaseaccountnames | × | × |
> | databaseaccounts | ○ | ○ |
> | locations | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / operationresults | × | × |
> | locations / operationsstatus | × | × |
> | operationresults | × | × |
> | operations | × | × |

## <a name="microsoftdomainregistration"></a>Microsoft.DomainRegistration

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checkdomainavailability | × | × |
> | domains | ○ | ○ |
> | domains / domainownershipidentifiers | × | × |
> | generatessorequest | × | × |
> | listdomainrecommendations | × | × |
> | operations | × | × |
> | topleveldomains | × | × |
> | validatedomainregistrationinformation | × | × |

## <a name="microsoftenterpriseknowledgegraph"></a>Microsoft.EnterpriseKnowledgeGraph

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |
> | services | ○ | ○ |

## <a name="microsofteventgrid"></a>Microsoft.EventGrid

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | domains | ○ | ○ |
> | domains / topics | × | × |
> | eventsubscriptions | × - 個別に移動できませんが、サブスクライブしたリソースで自動的に移動されます。 | × - 個別に移動できませんが、サブスクライブしたリソースで自動的に移動されます。 |
> | extensiontopics | × | × |
> | locations | × | × |
> | locations / eventsubscriptions | × | × |
> | locations / operationresults | × | × |
> | locations / operationsstatus | × | × |
> | locations / topictypes | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | operationsstatus | × | × |
> | partnernamespaces | ○ | ○ |
> | partnernamespaces / eventchannels | × | × |
> | partnerregistrations | × | × |
> | partnertopics | ○ | ○ |
> | partnertopics / eventsubscriptions | × | × |
> | systemtopics | ○ | ○ |
> | systemtopics / eventsubscriptions | × | × |
> | topics | ○ | ○ |
> | topictypes | × | × |

## <a name="microsofteventhub"></a>Microsoft.EventHub

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | availableclusterregions | × | × |
> | checknameavailability | × | × |
> | checknamespaceavailability | × | × |
> | clusters | ○ | ○ |
> | locations | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | namespaces | ○ | ○ |
> | namespaces / authorizationrules | × | × |
> | namespaces / disasterrecoveryconfigs | × | × |
> | namespaces / disasterrecoveryconfigs / checknameavailability | × | × |
> | namespaces / eventhubs | × | × |
> | namespaces / eventhubs / authorizationrules | × | × |
> | namespaces / eventhubs / consumergroups | × | × |
> | namespaces / networkrulesets | × | × |
> | operations | × | × |
> | sku | × | × |

## <a name="microsoftexperimentation"></a>Microsoft.Experimentation

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | experimentworkspaces | × | × |
> | locations | × | × |
> | locations / operations | × | × |

## <a name="microsoftfalcon"></a>Microsoft.Falcon

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | namespaces | ○ | ○ |

## <a name="microsoftfeatures"></a>Microsoft.Features

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | featureproviders | × | × |
> | features | × | × |
> | operations | × | × |
> | providers | × | × |
> | subscriptionfeatureregistrations | × | × |

## <a name="microsoftgenomics"></a>Microsoft.Genomics

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |

## <a name="microsoftguestconfiguration"></a>Microsoft.GuestConfiguration

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | automanagedaccounts | × | × |
> | automanagedvmconfigurationprofiles | × | × |
> | guestconfigurationassignments | × | × |
> | operations | × | × |
> | software | × | × |
> | softwareupdateprofile | × | × |
> | softwareupdates | × | × |

## <a name="microsofthanaonazure"></a>Microsoft.HanaOnAzure

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | hanainstances | × | × |
> | locations | × | × |
> | locations / operations | × | × |
> | locations / operationsstatus | × | × |
> | operations | × | × |
> | sapmonitors | ○ | ○ |

## <a name="microsofthardwaresecuritymodules"></a>Microsoft.HardwareSecurityModules

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | dedicatedhsms | × | × |
> | locations | × | × |
> | operations | × | × |

## <a name="microsofthdinsight"></a>Microsoft.HDInsight

> [!IMPORTANT]
> HDInsight クラスターは、新しいサブスクリプションまたはリソース グループに移動できます。 ただし、HDInsight クラスターにリンクされているネットワーク リソース (仮想ネットワーク、NIC、ロード バランサーなど) をサブスクリプション間で移動することはできません。 また、クラスターの仮想マシンに接続されている NIC を新しいリソース グループに移動することはできません。
>
> HDInsight クラスターを新しいサブスクリプションに移動するときは、まず、他のリソース (ストレージ アカウントなど) を移動します。 その後、HDInsight クラスターを単独で移動します。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | clusters | ○ | ○ |
> | clusters/applications | × | × |
> | clusters / operationresults | × | × |
> | locations | × | × |
> | locations / azureasyncoperations | × | × |
> | locations / billingspecs | × | × |
> | locations / capabilities | × | × |
> | locations / operationresults | × | × |
> | locations / usages | × | × |
> | locations / validatecreaterequest | × | × |
> | operations | × | × |

## <a name="microsofthealthcareapis"></a>Microsoft.HealthcareApis

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |
> | services | ○ | ○ |
> | services / privateendpointconnections | × | × |
> | services / privatelinkresources | × | × |

## <a name="microsofthybridcompute"></a>Microsoft.HybridCompute

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / operationresults | × | × |
> | locations / operationstatus | × | × |
> | machines | ○ | ○ |
> | machines / extensions | ○ | ○ |
> | operations | × | × |

## <a name="microsofthybriddata"></a>Microsoft.HybridData

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | datamanagers | ○ | ○ |
> | operations | × | × |

## <a name="microsofthybridnetwork"></a>Microsoft.HybridNetwork

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | devices | × | × |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | vnfs | × | × |

## <a name="microsofthydra"></a>Microsoft.Hydra

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | components | × | × |
> | locations | × | × |
> | networkscopes | × | × |
> | operations | × | × |

## <a name="microsoftimportexport"></a>Microsoft.ImportExport

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | jobs | ○ | ○ |
> | locations | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |

## <a name="microsoftinsights"></a>microsoft.insights

> [!IMPORTANT]
> 新しいサブスクリプションへの移動によって[サブスクリプション クォータ](azure-subscription-service-limits.md#azure-monitor-limits)を超えないようにします。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | actiongroups | ○ | ○ |
> | activitylogalerts | × | × |
> | alertrules | ○ | ○ |
> | autoscalesettings | ○ | ○ |
> | baseline | × | × |
> | calculatebaseline | × | × |
> | components | ○ | ○ |
> | components / events | × | × |
> | components / linkedstorageaccounts | × | × |
> | components / metadata | × | × |
> | components / metrics | × | × |
> | components / pricingplans | × | × |
> | components / query | × | × |
> | datacollectionrules | × | × |
> | diagnosticsettings | × | × |
> | diagnosticsettingscategories | × | × |
> | eventcategories | × | × |
> | eventtypes | × | × |
> | extendeddiagnosticsettings | × | × |
> | guestdiagnosticsettings | × | × |
> | listmigrationdate | × | × |
> | locations | × | × |
> | locations / operationresults | × | × |
> | logdefinitions | × | × |
> | logprofiles | × | × |
> | logs | × | × |
> | metricalerts | × | × |
> | metricbaselines | × | × |
> | metricbatch | × | × |
> | metricdefinitions | × | × |
> | metricnamespaces | × | × |
> | metrics | × | × |
> | migratealertrules | × | × |
> | migratetonewpricingmodel | × | × |
> | myworkbooks | × | × |
> | notificationgroups | × | × |
> | operations | × | × |
> | privatelinkscopeoperationstatuses | × | × |
> | privatelinkscopes | × | × |
> | privatelinkscopes / privateendpointconnectionproxies | × | × |
> | privatelinkscopes / privateendpointconnections | × | × |
> | privatelinkscopes / scopedresources | × | × |
> | rollbacktolegacypricingmodel | × | × |
> | scheduledqueryrules | ○ | ○ |
> | トポロジ | × | × |
> | トランザクション | × | × |
> | vminsightsonboardingstatuses | × | × |
> | webtests | ○ | ○ |
> | webtests / gettestresultfile | × | × |
> | Workbooks | ○ | ○ |
> | workbooktemplates | ○ | ○ |

## <a name="microsoftiotcentral"></a>Microsoft.IoTCentral

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | apptemplates | × | × |
> | checknameavailability | × | × |
> | checksubdomainavailability | × | × |
> | iotapps | ○ | ○ |
> | operations | × | × |

## <a name="microsoftiotspaces"></a>Microsoft.IoTSpaces

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | ○ | ○ |
> | graph | ○ | ○ |
> | operations | × | × |

## <a name="microsoftkeyvault"></a>Microsoft.KeyVault

> [!IMPORTANT]
> ディスクの暗号化に使用されるキー コンテナーは、同じサブスクリプション内のリソース グループに移動したり、サブスクリプション間で移動したりすることはできません。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | deletedvaults | × | × |
> | hsmpools | × | × |
> | locations | × | × |
> | locations / deletedvaults | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / operationresults | × | × |
> | managedhsms | × | × |
> | operations | × | × |
> | vaults | ○ | ○ |
> | vaults / accesspolicies | × | × |
> | vaults / eventgridfilters | × | × |
> | vaults / secrets | × | × |

## <a name="microsoftkubernetes"></a>Microsoft.Kubernetes

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | connectedclusters | ○ | ○ |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | registeredsubscriptions | × | × |

## <a name="microsoftkubernetesconfiguration"></a>Microsoft.KubernetesConfiguration

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | sourcecontrolconfigurations | × | × |

## <a name="microsoftkusto"></a>Microsoft.Kusto

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | clusters | ○ | ○ |
> | clusters / attacheddatabaseconfigurations | × | × |
> | clusters / databases | × | × |
> | clusters / databases / dataconnections | × | × |
> | clusters / databases / eventhubconnections | × | × |
> | clusters / databases / principalassignments | × | × |
> | clusters / principalassignments | × | × |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | operations | × | × |

## <a name="microsoftlabservices"></a>Microsoft.LabServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | labaccounts | × | × |
> | locations | × | × |
> | locations / operations | × | × |
> | operations | × | × |
> | users | × | × |

## <a name="microsoftlocationbasedservices"></a>Microsoft.LocationBasedServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |

## <a name="microsoftlocationservices"></a>Microsoft.LocationServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |

## <a name="microsoftlogic"></a>Microsoft.Logic

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | hostingenvironments | × | × |
> | integrationaccounts | ○ | ○ |
> | integrationserviceenvironments | ○ | × |
> | integrationserviceenvironments / managedapis | ○ | × |
> | isolatedenvironments | × | × |
> | locations | × | × |
> | locations / workflows | × | × |
> | operations | × | × |
> | workflows | ○ | ○ |

## <a name="microsoftmachinelearning"></a>Microsoft.MachineLearning

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | commitmentplans | × | × |
> | locations | × | × |
> | locations / operations | × | × |
> | locations / operationsstatus | × | × |
> | operations | × | × |
> | webservices | ○ | × |
> | workspaces | ○ | ○ |

## <a name="microsoftmachinelearningcompute"></a>Microsoft.MachineLearningCompute

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operationalizationclusters | × | × |

## <a name="microsoftmachinelearningexperimentation"></a>Microsoft.MachineLearningExperimentation

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |
> | accounts/workspaces | × | × |
> | accounts/workspaces/projects | × | × |
> | teamaccounts | × | × |
> | teamaccounts/workspaces | × | × |
> | teamaccounts/workspaces/projects | × | × |

## <a name="microsoftmachinelearningmodelmanagement"></a>Microsoft.MachineLearningModelManagement

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |

## <a name="microsoftmachinelearningservices"></a>Microsoft.MachineLearningServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / computeoperationsstatus | × | × |
> | locations / quotas | × | × |
> | locations / updatequotas | × | × |
> | locations / usages | × | × |
> | locations / vmsizes | × | × |
> | locations / workspaceoperationsstatus | × | × |
> | operations | × | × |
> | workspaces | × | × |
> | workspaces / computes | × | × |
> | workspaces / eventgridfilters | × | × |

## <a name="microsoftmaintenance"></a>Microsoft.Maintenance

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applyupdates | × | × |
> | configurationassignments | × | × |
> | maintenanceconfigurations | ○ | ○ |
> | updates | × | × |

## <a name="microsoftmanagedidentity"></a>Microsoft.ManagedIdentity

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | ID | × | × |
> | operations | × | × |
> | userassignedidentities | × | × |

## <a name="microsoftmanagednetwork"></a>Microsoft.ManagedNetwork

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | managednetworks | × | × |
> | managednetworks / managednetworkgroups | × | × |
> | managednetworks / managednetworkpeeringpolicies | × | × |
> | 通知 (notification) | × | × |

## <a name="microsoftmanagedservices"></a>Microsoft.ManagedServices

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | marketplaceregistrationdefinitions | × | × |
> | operations | × | × |
> | operationstatuses | × | × |
> | registrationassignments | × | × |
> | registrationdefinitions | × | × |

## <a name="microsoftmanagement"></a>Microsoft.Management

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | getentities | × | × |
> | managementgroups | × | × |
> | managementgroups / settings | × | × |
> | operationresults | × | × |
> | operationresults / asyncoperation | × | × |
> | operations | × | × |
> | resources | × | × |
> | starttenantbackfill | × | × |
> | tenantbackfillstatus | × | × |

## <a name="microsoftmaps"></a>Microsoft.Maps

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | ○ | ○ |
> | accounts / eventgridfilters | × | × |
> | accounts / privateatlases | ○ | ○ |
> | operations | × | × |

## <a name="microsoftmarketplace"></a>Microsoft.Marketplace

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | listavailableoffers | × | × |
> | offers | × | × |
> | offertypes | × | × |
> | offertypes / publishers | × | × |
> | offertypes / publishers / offers | × | × |
> | offertypes / publishers / offers / plans | × | × |
> | offertypes / publishers / offers / plans / agreements | × | × |
> | offertypes / publishers / offers / plans / configs | × | × |
> | offertypes / publishers / offers / plans / configs / importimage | × | × |
> | operations | × | × |
> | privategalleryitems | × | × |
> | privatestoreclient | × | × |
> | privatestores | × | × |
> | privatestores / offers | × | × |
> | products | × | × |
> | publishers | × | × |
> | publishers / offers | × | × |
> | publishers / offers / amendments | × | × |
> | registrations | × | × |

## <a name="microsoftmarketplaceapps"></a>Microsoft.MarketplaceApps

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | classicdevservices | × | × |
> | listcommunicationpreference | × | × |
> | operations | × | × |
> | updatecommunicationpreference | × | × |

## <a name="microsoftmarketplaceordering"></a>Microsoft.MarketplaceOrdering

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | agreements | × | × |
> | offertypes | × | × |
> | operations | × | × |

## <a name="microsoftmedia"></a>Microsoft.Media

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | mediaservices | ○ | ○ |
> | mediaservices / accountfilters | × | × |
> | mediaservices / assets | × | × |
> | mediaservices / assets / assetfilters | × | × |
> | mediaservices / contentkeypolicies | × | × |
> | mediaservices / eventgridfilters | × | × |
> | mediaservices / liveeventoperations | × | × |
> | mediaservices/liveevents | ○ | ○ |
> | mediaservices / liveevents / liveoutputs | × | × |
> | mediaservices / liveoutputoperations | × | × |
> | mediaservices / streamingendpointoperations | × | × |
> | mediaservices/streamingendpoints | ○ | ○ |
> | mediaservices / streaminglocators | × | × |
> | mediaservices / streamingpolicies | × | × |
> | mediaservices / transforms | × | × |
> | mediaservices / transforms / jobs | × | × |
> | operations | × | × |

## <a name="microsoftmicroservices4spring"></a>Microsoft.Microservices4Spring

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | appclusters | × | × |

## <a name="microsoftmigrate"></a>Microsoft.Migrate

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | assessmentprojects | × | × |
> | locations | × | × |
> | locations / assessmentoptions | × | × |
> | locations / checknameavailability | × | × |
> | migrateprojects | × | × |
> | movecollections | × | × |
> | operations | × | × |
> | projects | × | × |

## <a name="microsoftmixedreality"></a>Microsoft.MixedReality

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | holographicsbroadcastaccounts | × | × |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | objectunderstandingaccounts | × | × |
> | operations | × | × |
> | remoterenderingaccounts | ○ | ○ |
> | spatialanchorsaccounts | ○ | ○ |

## <a name="microsoftnetapp"></a>Microsoft.NetApp

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | netappaccounts | × | × |
> | netappaccounts/backuppolicies | × | × |
> | netappaccounts/capacitypools | × | × |
> | netappaccounts/capacitypools/volumes | × | × |
> | netappaccounts/capacitypools/volumes/mounttargets | × | × |
> | netappaccounts/capacitypools/volumes/snapshots | × | × |
> | operations | × | × |

## <a name="microsoftnetwork"></a>Microsoft.Network

> [!IMPORTANT]
> [ネットワークの移動ガイダンス](./move-limitations/networking-move-limitations.md)をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applicationgatewayavailablerequestheaders | × | × |
> | applicationgatewayavailableresponseheaders | × | × |
> | applicationgatewayavailableservervariables | × | × |
> | applicationgatewayavailablessloptions | × | × |
> | applicationgatewayavailablewafrulesets | × | × |
> | applicationgateways | × | × |
> | applicationgatewaywebapplicationfirewallpolicies | × | × |
> | applicationsecuritygroups | ○ | ○ |
> | azurefirewallfqdntags | × | × |
> | azurefirewalls | × | × |
> | bastionhosts | × | × |
> | bgpservicecommunities | × | × |
> | checkfrontdoornameavailability | × | × |
> | checktrafficmanagernameavailability | × | × |
> | connections | ○ | ○ |
> | ddoscustompolicies | ○ | ○ |
> | ddosprotectionplans | × | × |
> | dnsoperationresults | × | × |
> | dnsoperationstatuses | × | × |
> | dnszones | ○ | ○ |
> | dnszones/a | × | × |
> | dnszones/aaaa | × | × |
> | dnszones / all | × | × |
> | dnszones / caa | × | × |
> | dnszones/cname | × | × |
> | dnszones/mx | × | × |
> | dnszones / ns | × | × |
> | dnszones/ptr | × | × |
> | dnszones / recordsets | × | × |
> | dnszones / soa | × | × |
> | dnszones/srv | × | × |
> | dnszones/txt | × | × |
> | expressroutecircuits | × | × |
> | expressroutegateways | × | × |
> | expressrouteserviceproviders | × | × |
> | firewallpolicies | ○ | ○ |
> | frontdooroperationresults | × | × |
> | frontdoors | × | × |
> | frontdoors / frontendendpoints | × | × |
> | frontdoorwebapplicationfirewallmanagedrulesets | × | × |
> | frontdoorwebapplicationfirewallpolicies | × | × |
> | getdnsresourcereference | × | × |
> | internalnotify | × | × |
> | ipallocations | ○ | ○ |
> | ipgroups | ○ | ○ |
> | loadbalancers | ○ - Basic SKU<br>× - Standard SKU | ○ - Basic SKU<br>× - Standard SKU |
> | localnetworkgateways | ○ | ○ |
> | locations | × | × |
> | locations / autoapprovedprivatelinkservices | × | × |
> | locations / availabledelegations | × | × |
> | locations / availableprivateendpointtypes | × | × |
> | locations / availableservicealiases | × | × |
> | locations / baremetaltenants | × | × |
> | locations / batchnotifyprivateendpointsforresourcemove | × | × |
> | locations / batchvalidateprivateendpointsforresourcemove | × | × |
> | locations / checkacceleratednetworkingsupport | × | × |
> | locations / checkdnsnameavailability | × | × |
> | locations / checkprivatelinkservicevisibility | × | × |
> | locations / commitinternalazurenetworkmanagerconfiguration | × | × |
> | locations / effectiveresourceownership | × | × |
> | locations / nfvoperationresults | × | × |
> | locations / nfvoperations | × | × |
> | locations / operationresults | × | × |
> | locations / operations | × | × |
> | locations / servicetags | × | × |
> | locations / setresourceownership | × | × |
> | locations / supportedvirtualmachinesizes | × | × |
> | locations / usages | × | × |
> | locations / validateresourceownership | × | × |
> | locations / virtualnetworkavailableendpointservices | × | × |
> | natgateways | × | × |
> | networkexperimentprofiles | × | × |
> | networkintentpolicies | ○ | ○ |
> | networkinterfaces | ○ | ○ |
> | networkprofiles | × | × |
> | networksecuritygroups | ○ | ○ |
> | networkwatchers | ○ | × |
> | networkwatchers/connectionmonitors | ○ | × |
> | networkwatchers/flowlogs | ○ | × |
> | networkwatchers/pingmeshes | ○ | × |
> | operations | × | × |
> | p2svpngateways | × | × |
> | privatednsoperationresults | × | × |
> | privatednsoperationstatuses | × | × |
> | privatednszones | ○ | ○ |
> | privatednszones / a | × | × |
> | privatednszones / aaaa | × | × |
> | privatednszones / all | × | × |
> | privatednszones / cname | × | × |
> | privatednszones / mx | × | × |
> | privatednszones / ptr | × | × |
> | privatednszones / soa | × | × |
> | privatednszones / srv | × | × |
> | privatednszones / txt | × | × |
> | privatednszones/virtualnetworklinks | ○ | ○ |
> | privatednszonesinternal | × | × |
> | privateendpointredirectmaps | × | × |
> | privateendpoints | ○ | ○ |
> | privatelinkservices | × | × |
> | publicipaddresses | ○ - Basic SKU<br>× - Standard SKU | ○ - Basic SKU<br>× - Standard SKU |
> | publicipprefixes | ○ | ○ |
> | routefilters | × | × |
> | routetables | ○ | ○ |
> | securitypartnerproviders | ○ | ○ |
> | serviceendpointpolicies | ○ | ○ |
> | trafficmanagergeographichierarchies | × | × |
> | trafficmanagerprofiles | ○ | ○ |
> | trafficmanagerprofiles / heatmaps | × | × |
> | trafficmanagerusermetricskeys | × | × |
> | virtualhubs | × | × |
> | virtualnetworkgateways | ○ | ○ |
> | virtualnetworks | ○ | ○ |
> | virtualnetworktaps | × | × |
> | virtualrouters | ○ | ○ |
> | virtualwans | × | × |
> | vpngateways (仮想 WAN) | × | × |
> | vpnserverconfigurations | × | × |
> | vpnsites (仮想 WAN) | × | × |

## <a name="microsoftnotificationhubs"></a>Microsoft.NotificationHubs

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | checknamespaceavailability | × | × |
> | namespaces | ○ | ○ |
> | namespaces/notificationhubs | ○ | ○ |
> | operationresults | × | × |
> | operations | × | × |

## <a name="microsoftobjectstore"></a>Microsoft.ObjectStore

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | osnamespaces | ○ | ○ |

## <a name="microsoftoffazure"></a>Microsoft.OffAzure

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | hypervsites | × | × |
> | importsites | × | × |
> | operations | × | × |
> | serversites | × | × |
> | vmwaresites | × | × |

## <a name="microsoftoperationalinsights"></a>Microsoft.OperationalInsights

> [!IMPORTANT]
> 新しいサブスクリプションへの移行によって、[サブスクリプション クォータ](azure-subscription-service-limits.md#azure-monitor-limits)が超えることがないようにします。
>
> Automation アカウントがリンクされているワークスペースは移動できません。 移動操作を開始する前に、リンクされている Automation アカウントは必ず解除してください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | clusters | × | × |
> | deletedworkspaces | × | × |
> | linktargets | × | × |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | storageinsightconfigs | × | × |
> | workspaces | ○ | ○ |
> | workspaces / datasources | × | × |
> | workspaces / linkedservices | × | × |
> | workspaces / linkedstorageaccounts | × | × |
> | workspaces / metadata | × | × |
> | workspaces / query | × | × |
> | workspaces / scopedprivatelinkproxies | × | × |

## <a name="microsoftoperationsmanagement"></a>Microsoft.OperationsManagement

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | managementassociations | × | × |
> | managementconfigurations | ○ | ○ |
> | operations | × | × |
> | solutions | ○ | ○ |
> | views | ○ | ○ |

## <a name="microsoftpeering"></a>Microsoft.Peering

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checkserviceprovideravailability | × | × |
> | legacypeerings | × | × |
> | operations | × | × |
> | peerasns | × | × |
> | peeringlocations | × | × |
> | peerings | × | × |
> | peeringservicecountries | × | × |
> | peeringservicelocations | × | × |
> | peeringserviceproviders | × | × |
> | peeringservices | × | × |

## <a name="microsoftpolicyinsights"></a>Microsoft.PolicyInsights

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | asyncoperationresults | × | × |
> | operations | × | × |
> | policyevents | × | × |
> | policystates | × | × |
> | policytrackedresources | × | × |
> | remediations | × | × |

## <a name="microsoftportal"></a>Microsoft.Portal

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | consoles | × | × |
> | dashboards | ○ | ○ |
> | locations | × | × |
> | locations / consoles | × | × |
> | locations / usersettings | × | × |
> | operations | × | × |
> | usersettings | × | × |

## <a name="microsoftpowerbi"></a>Microsoft.PowerBI

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | workspacecollections | ○ | ○ |

## <a name="microsoftpowerbidedicated"></a>Microsoft.PowerBIDedicated

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | capacities | ○ | ○ |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |

## <a name="microsoftpowerplatform"></a>Microsoft.PowerPlatform

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |

## <a name="microsoftprojectbabylon"></a>Microsoft.ProjectBabylon

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |
> | checknameavailability | × | × |
> | operations | × | × |

## <a name="microsoftproviderhub"></a>Microsoft.ProviderHub

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | availableaccounts | × | × |
> | providerregistrations | × | × |
> | providerregistrations / resourcetyperegistrations | × | × |
> | rollouts | × | × |

## <a name="microsoftquantum"></a>Microsoft.Quantum

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | workspaces | × | × |

## <a name="microsoftrecoveryservices"></a>Microsoft.RecoveryServices

> [!IMPORTANT]
> [Recovery Services の移動のガイダンス](../../backup/backup-azure-move-recovery-services-vault.md?toc=/azure/azure-resource-manager/toc.json)に関する記事をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | backupprotecteditems | × | × |
> | locations | × | × |
> | locations / allocatedstamp | × | × |
> | locations / allocatestamp | × | × |
> | locations / backupaadproperties | × | × |
> | locations / backupcrossregionrestore | × | × |
> | locations / backupcrrjob | × | × |
> | locations / backupcrrjobs | × | × |
> | locations / backupcrroperationresults | × | × |
> | locations / backupcrroperationsstatus | × | × |
> | locations / backupprevalidateprotection | × | × |
> | locations / backupstatus | × | × |
> | locations / backupvalidatefeatures | × | × |
> | locations / checknameavailability | × | × |
> | operations | × | × |
> | replicationeligibilityresults | × | × |
> | vaults | ○ | ○ |

## <a name="microsoftredhatopenshift"></a>Microsoft.RedHatOpenShift

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / operationresults | × | × |
> | locations / operationsstatus | × | × |
> | openshiftclusters | × | × |
> | operations | × | × |

## <a name="microsoftrelay"></a>Microsoft.Relay

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | namespaces | ○ | ○ |
> | namespaces / authorizationrules | × | × |
> | namespaces / hybridconnections | × | × |
> | namespaces / hybridconnections / authorizationrules | × | × |
> | namespaces / privateendpointconnections | × | × |
> | namespaces / wcfrelays | × | × |
> | namespaces / wcfrelays / authorizationrules | × | × |
> | operations | × | × |

## <a name="microsoftresourcegraph"></a>Microsoft.ResourceGraph

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | operations | × | × |
> | Query | ○ | ○ |
> | resourcechangedetails | × | × |
> | resourcechanges | × | × |
> | resources | × | × |
> | resourceshistory | × | × |
> | subscriptionsstatus | × | × |

## <a name="microsoftresourcehealth"></a>Microsoft.ResourceHealth

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | availabilitystatuses | × | × |
> | childavailabilitystatuses | × | × |
> | childresources | × | × |
> | emergingissues | × | × |
> | events | × | × |
> | metadata | × | × |
> | notifications | × | × |
> | operations | × | × |

## <a name="microsoftresources"></a>Microsoft.Resources

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | calculatetemplatehash | × | × |
> | checkpolicycompliance | × | × |
> | checkresourcename | × | × |
> | deployments | × | × |
> | deployments / operations | × | × |
> | deploymentscripts | × | × |
> | deploymentscripts / logs | × | × |
> | リンク | × | × |
> | locations | × | × |
> | locations / deploymentscriptoperationresults | × | × |
> | notifyresourcejobs | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | providers | × | × |
> | resourcegroups | × | × |
> | resources | × | × |
> | subscriptions | × | × |
> | subscriptions / locations | × | × |
> | subscriptions / operationresults | × | × |
> | subscriptions / providers | × | × |
> | subscriptions / resourcegroups | × | × |
> | subscriptions / resourcegroups / resources | × | × |
> | subscriptions / resources | × | × |
> | subscriptions / tagnames | × | × |
> | subscriptions / tagnames / tagvalues | × | × |
> | tags | × | × |
> | templatespecs | × | × |
> | templatespecs / versions | × | × |
> | tenants | × | × |

## <a name="microsoftsaas"></a>Microsoft.SaaS

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applications | ○ | × |
> | checkmoderneligibility | × | × |
> | checknameavailability | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | saasresources | × | × |

## <a name="microsoftsearch"></a>Microsoft.Search

> [!IMPORTANT]
> 1 回の操作で異なるリージョンにあるいくつかの Search リソースを一度に移動することはできません。 代わりに、別の操作で移動します。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | checkservicenameavailability | × | × |
> | operations | × | × |
> | resourcehealthmetadata | × | × |
> | searchservices | ○ | ○ |

## <a name="microsoftsecurity"></a>Microsoft.Security

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | adaptivenetworkhardenings | × | × |
> | advancedthreatprotectionsettings | × | × |
> | alerts | × | × |
> | allowedconnections | × | × |
> | applicationwhitelistings | × | × |
> | assessmentmetadata | × | × |
> | assessments | × | × |
> | autodismissalertsrules | × | × |
> | automations | ○ | ○ |
> | autoprovisioningsettings | × | × |
> | complianceresults | × | × |
> | compliances | × | × |
> | datacollectionagents | × | × |
> | devicesecuritygroups | × | × |
> | discoveredsecuritysolutions | × | × |
> | externalsecuritysolutions | × | × |
> | informationprotectionpolicies | × | × |
> | iotsecuritysolutions | ○ | ○ |
> | iotsecuritysolutions / analyticsmodels | × | × |
> | iotsecuritysolutions / analyticsmodels / aggregatedalerts | × | × |
> | iotsecuritysolutions / analyticsmodels / aggregatedrecommendations | × | × |
> | jitnetworkaccesspolicies | × | × |
> | locations | × | × |
> | locations / alerts | × | × |
> | locations / allowedconnections | × | × |
> | locations / applicationwhitelistings | × | × |
> | locations / discoveredsecuritysolutions | × | × |
> | locations / externalsecuritysolutions | × | × |
> | locations / jitnetworkaccesspolicies | × | × |
> | locations / securitysolutions | × | × |
> | locations / securitysolutionsreferencedata | × | × |
> | locations / tasks | × | × |
> | locations / topologies | × | × |
> | operations | × | × |
> | policies | × | × |
> | pricings | × | × |
> | regulatorycompliancestandards | × | × |
> | regulatorycompliancestandards / regulatorycompliancecontrols | × | × |
> | regulatorycompliancestandards / regulatorycompliancecontrols / regulatorycomplianceassessments | × | × |
> | securitycontacts | × | × |
> | securitysolutions | × | × |
> | securitysolutionsreferencedata | × | × |
> | securitystatuses | × | × |
> | securitystatusessummaries | × | × |
> | servervulnerabilityassessments | × | × |
> | settings | × | × |
> | subassessments | × | × |
> | tasks | × | × |
> | topologies | × | × |
> | workspacesettings | × | × |

## <a name="microsoftsecurityinsights"></a>Microsoft.SecurityInsights

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | aggregations | × | × |
> | alertrules | × | × |
> | alertruletemplates | × | × |
> | automationrules | × | × |
> | bookmarks | × | × |
> | cases | × | × |
> | dataconnectors | × | × |
> | dataconnectorscheckrequirements | × | × |
> | entities | × | × |
> | entityqueries | × | × |
> | incidents | × | × |
> | officeconsents | × | × |
> | operations | × | × |
> | settings | × | × |
> | threatintelligence | × | × |

## <a name="microsoftserialconsole"></a>Microsoft.SerialConsole

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | consoleservices | × | × |
> | locations | × | × |
> | locations / consoleservices | × | × |
> | operations | × | × |

## <a name="microsoftservermanagement"></a>Microsoft.ServerManagement

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | gateways | × | × |
> | nodes | × | × |

## <a name="microsoftservicebus"></a>Microsoft.ServiceBus

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | checknamespaceavailability | × | × |
> | locations | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | namespaces | ○ | ○ |
> | namespaces / authorizationrules | × | × |
> | namespaces / disasterrecoveryconfigs | × | × |
> | namespaces / disasterrecoveryconfigs / checknameavailability | × | × |
> | namespaces / eventgridfilters | × | × |
> | namespaces / networkrulesets | × | × |
> | namespaces / queues | × | × |
> | namespaces / queues / authorizationrules | × | × |
> | namespaces / topics | × | × |
> | namespaces / topics / authorizationrules | × | × |
> | namespaces / topics / subscriptions | × | × |
> | namespaces / topics / subscriptions / rules | × | × |
> | operations | × | × |
> | premiummessagingregions | × | × |
> | sku | × | × |

## <a name="microsoftservicefabric"></a>Microsoft.ServiceFabric

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applications | × | × |
> | clusters | ○ | ○ |
> | clusters/applications | × | × |
> | containergroups | × | × |
> | containergroupsets | × | × |
> | edgeclusters | × | × |
> | locations | × | × |
> | locations / clusterversions | × | × |
> | locations / environments | × | × |
> | locations / operationresults | × | × |
> | locations / operations | × | × |
> | managedclusters | × | × |
> | networks | × | × |
> | operations | × | × |
> | secretstores | × | × |
> | volumes | × | × |

## <a name="microsoftservicefabricmesh"></a>Microsoft.ServiceFabricMesh

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applications | ○ | ○ |
> | containergroups | × | × |
> | gateways | ○ | ○ |
> | locations | × | × |
> | locations / applicationoperations | × | × |
> | locations / gatewayoperations | × | × |
> | locations / networkoperations | × | × |
> | locations / secretoperations | × | × |
> | locations / volumeoperations | × | × |
> | networks | ○ | ○ |
> | operations | × | × |
> | secrets | ○ | ○ |
> | volumes | ○ | ○ |

## <a name="microsoftservices"></a>Microsoft.Services

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | rollouts | × | × |

## <a name="microsoftsignalrservice"></a>Microsoft.SignalRService

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / operationstatuses | × | × |
> | locations / usages | × | × |
> | operations | × | × |
> | signalr | ○ | ○ |
> | signalr / eventgridfilters | × | × |

## <a name="microsoftsoftwareplan"></a>Microsoft.SoftwarePlan

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | hybridusebenefits | × | × |
> | operations | × | × |

## <a name="microsoftsolutions"></a>Microsoft.Solutions

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | applicationdefinitions | × | × |
> | applications | × | × |
> | jitrequests | × | × |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |

## <a name="microsoftsql"></a>Microsoft.Sql

> [!IMPORTANT]
> データベースとサーバーは同じリソース グループ内に存在する必要があります。 SQL Server を移動すると、そのデータベースもすべて移動されます。 この動作は、Azure SQL Database と Azure Synapse Analytics データベースに適用されます。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | instancepools | × | × |
> | locations | ○ | ○ |
> | locations / administratorazureasyncoperation | × | × |
> | locations / administratoroperationresults | × | × |
> | locations / auditingsettingsazureasyncoperation | × | × |
> | locations / auditingsettingsoperationresults | × | × |
> | locations / capabilities | × | × |
> | locations / databaseazureasyncoperation | × | × |
> | locations / databaseoperationresults | × | × |
> | locations / databaserestoreazureasyncoperation | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / deletevirtualnetworkorsubnetsazureasyncoperation | × | × |
> | locations / deletevirtualnetworkorsubnetsoperationresults | × | × |
> | locations / dnsaliasasyncoperation | × | × |
> | locations / dnsaliasoperationresults | × | × |
> | locations / elasticpoolazureasyncoperation | × | × |
> | locations / elasticpooloperationresults | × | × |
> | locations / encryptionprotectorazureasyncoperation | × | × |
> | locations / encryptionprotectoroperationresults | × | × |
> | locations / extendedauditingsettingsazureasyncoperation | × | × |
> | locations / extendedauditingsettingsoperationresults | × | × |
> | locations / failovergroupazureasyncoperation | × | × |
> | locations / failovergroupoperationresults | × | × |
> | locations / firewallrulesazureasyncoperation | × | × |
> | locations / firewallrulesoperationresults | × | × |
> | locations / instancefailovergroupazureasyncoperation | × | × |
> | locations / instancefailovergroupoperationresults | × | × |
> | locations / instancefailovergroups | × | × |
> | locations / instancepoolazureasyncoperation | × | × |
> | locations / instancepooloperationresults | × | × |
> | locations / jobagentazureasyncoperation | × | × |
> | locations / jobagentoperationresults | × | × |
> | locations / longtermretentionbackupazureasyncoperation | × | × |
> | locations / longtermretentionbackupoperationresults | × | × |
> | locations / longtermretentionbackups | × | × |
> | locations / longtermretentionmanagedinstancebackupazureasyncoperation | × | × |
> | locations / longtermretentionmanagedinstancebackupoperationresults | × | × |
> | locations / longtermretentionmanagedinstancebackups | × | × |
> | locations / longtermretentionmanagedinstances | × | × |
> | locations / longtermretentionpolicyazureasyncoperation | × | × |
> | locations / longtermretentionpolicyoperationresults | × | × |
> | locations / longtermretentionservers | × | × |
> | locations / manageddatabaseazureasyncoperation | × | × |
> | locations / manageddatabasecompleterestoreazureasyncoperation | × | × |
> | locations / manageddatabasecompleterestoreoperationresults | × | × |
> | locations / manageddatabaseoperationresults | × | × |
> | locations / manageddatabaserestoreazureasyncoperation | × | × |
> | locations / manageddatabaserestoreoperationresults | × | × |
> | locations / managedinstanceazureasyncoperation | × | × |
> | locations / managedinstanceencryptionprotectorazureasyncoperation | × | × |
> | locations / managedinstanceencryptionprotectoroperationresults | × | × |
> | locations / managedinstancekeyazureasyncoperation | × | × |
> | locations / managedinstancekeyoperationresults | × | × |
> | locations / managedinstancelongtermretentionpolicyazureasyncoperation | × | × |
> | locations / managedinstancelongtermretentionpolicyoperationresults | × | × |
> | locations / managedinstanceoperationresults | × | × |
> | locations / managedinstancetdecertazureasyncoperation | × | × |
> | locations / managedinstancetdecertoperationresults | × | × |
> | locations / managedserversecurityalertpoliciesazureasyncoperation | × | × |
> | locations / managedserversecurityalertpoliciesoperationresults | × | × |
> | locations / managedshorttermretentionpolicyazureasyncoperation | × | × |
> | locations / managedshorttermretentionpolicyoperationresults | × | × |
> | locations / notifyazureasyncoperation | × | × |
> | locations / privateendpointconnectionazureasyncoperation | × | × |
> | locations / privateendpointconnectionoperationresults | × | × |
> | locations / privateendpointconnectionproxyazureasyncoperation | × | × |
> | locations / privateendpointconnectionproxyoperationresults | × | × |
> | locations / securityalertpoliciesazureasyncoperation | × | × |
> | locations / securityalertpoliciesoperationresults | × | × |
> | locations / serveradministratorazureasyncoperation | × | × |
> | locations / serveradministratoroperationresults | × | × |
> | locations / serverazureasyncoperation | × | × |
> | locations / serverkeyazureasyncoperation | × | × |
> | locations / serverkeyoperationresults | × | × |
> | locations / serveroperationresults | × | × |
> | locations / shorttermretentionpolicyazureasyncoperation | × | × |
> | locations / shorttermretentionpolicyoperationresults | × | × |
> | locations / syncagentoperationresults | × | × |
> | locations / syncdatabaseids | × | × |
> | locations / syncgroupoperationresults | × | × |
> | locations / syncmemberoperationresults | × | × |
> | locations / tdecertazureasyncoperation | × | × |
> | locations / tdecertoperationresults | × | × |
> | locations / usages | × | × |
> | locations / virtualclusterazureasyncoperation | × | × |
> | locations / virtualclusteroperationresults | × | × |
> | locations / virtualnetworkrulesazureasyncoperation | × | × |
> | locations / virtualnetworkrulesoperationresults | × | × |
> | locations / vulnerabilityassessmentscanazureasyncoperation | × | × |
> | locations / vulnerabilityassessmentscanoperationresults | × | × |
> | managedinstances | × | × |
> | managedinstances / administrators | × | × |
> | managedinstances/databases | × | × |
> | managedinstances / databases / backuplongtermretentionpolicies | × | × |
> | managedinstances / databases / vulnerabilityassessments | × | × |
> | managedinstances / metricdefinitions | × | × |
> | managedinstances / metrics | × | × |
> | managedinstances / recoverabledatabases | × | × |
> | managedinstances / tdecertificates | × | × |
> | managedinstances / vulnerabilityassessments | × | × |
> | operations | × | × |
> | servers | ○ | ○ |
> | servers / administratoroperationresults | × | × |
> | servers / administrators | × | × |
> | servers / advisors | × | × |
> | servers / aggregateddatabasemetrics | × | × |
> | servers / auditingpolicies | × | × |
> | servers / auditingsettings | × | × |
> | servers / automatictuning | × | × |
> | servers / communicationlinks | × | × |
> | servers / connectionpolicies | × | × |
> | servers/databases | ○ | ○ |
> | servers / databases / advisors | × | × |
> | servers / databases / auditingpolicies | × | × |
> | servers / databases / auditingsettings | × | × |
> | servers / databases / auditrecords | × | × |
> | servers / databases / automatictuning | × | × |
> | servers / databases / backuplongtermretentionpolicies | × | × |
> | servers / databases / backupshorttermretentionpolicies | × | × |
> | servers / databases / connectionpolicies | × | × |
> | servers / databases / datamaskingpolicies | × | × |
> | servers / databases / datamaskingpolicies / rules | × | × |
> | servers / databases / extensions | × | × |
> | servers / databases / geobackuppolicies | × | × |
> | servers / databases / metricdefinitions | × | × |
> | servers / databases / metrics | × | × |
> | servers / databases / recommendedsensitivitylabels | × | × |
> | servers / databases / securityalertpolicies | × | × |
> | servers / databases / syncgroups | × | × |
> | servers / databases / syncgroups / syncmembers | × | × |
> | servers / databases / topqueries | × | × |
> | servers / databases / topqueries / querytext | × | × |
> | servers / databases / transparentdataencryption | × | × |
> | servers / databases / vulnerabilityassessment | × | × |
> | servers / databases / vulnerabilityassessments | × | × |
> | servers / databases / vulnerabilityassessmentscans | × | × |
> | servers / databases / vulnerabilityassessmentsettings | × | × |
> | servers / databases / workloadgroups | × | × |
> | servers / databasesecuritypolicies | × | × |
> | servers / disasterrecoveryconfiguration | × | × |
> | servers / dnsaliases | × | × |
> | servers / elasticpoolestimates | × | × |
> | servers/elasticpools | ○ | ○ |
> | servers / elasticpools / advisors | × | × |
> | servers / elasticpools / metricdefinitions | × | × |
> | servers / elasticpools / metrics | × | × |
> | servers / encryptionprotector | × | × |
> | servers / extendedauditingsettings | × | × |
> | servers / failovergroups | × | × |
> | servers / import | × | × |
> | servers / importexportoperationresults | × | × |
> | servers/jobaccounts | ○ | ○ |
> | servers/jobagents | ○ | ○ |
> | servers / jobagents / jobs | × | × |
> | servers / jobagents / jobs / executions | × | × |
> | servers / jobagents / jobs / steps | × | × |
> | servers / keys | × | × |
> | servers / operationresults | × | × |
> | servers / recommendedelasticpools | × | × |
> | servers / recoverabledatabases | × | × |
> | servers / restorabledroppeddatabases | × | × |
> | servers / securityalertpolicies | × | × |
> | servers / serviceobjectives | × | × |
> | servers / syncagents | × | × |
> | servers / tdecertificates | × | × |
> | servers / usages | × | × |
> | servers / virtualnetworkrules | × | × |
> | servers / vulnerabilityassessments | × | × |
> | virtualclusters | ○ | ○ |

## <a name="microsoftsqlvirtualmachine"></a>Microsoft.SqlVirtualMachine

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / availabilitygrouplisteneroperationresults | × | × |
> | locations / operationtypes | × | × |
> | locations / sqlvirtualmachinegroupoperationresults | × | × |
> | locations / sqlvirtualmachineoperationresults | × | × |
> | operations | × | × |
> | sqlvirtualmachinegroups | ○ | ○ |
> | sqlvirtualmachinegroups / availabilitygrouplisteners | × | × |
> | sqlvirtualmachines | ○ | ○ |

## <a name="microsoftstorage"></a>Microsoft.Storage

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | locations | × | × |
> | locations / asyncoperations | × | × |
> | locations / checknameavailability | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / usages | × | × |
> | operations | × | × |
> | storageaccounts | ○ | ○ |
> | storageaccounts / blobservices | × | × |
> | storageaccounts / fileservices | × | × |
> | storageaccounts / listaccountsas | × | × |
> | storageaccounts / listservicesas | × | × |
> | storageaccounts / queueservices | × | × |
> | storageaccounts / services | × | × |
> | storageaccounts / services / metricdefinitions | × | × |
> | storageaccounts / tableservices | × | × |
> | usages | × | × |

## <a name="microsoftstoragecache"></a>Microsoft.StorageCache

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | caches | × | × |

## <a name="microsoftstoragesync"></a>Microsoft.StorageSync

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / checknameavailability | × | × |
> | locations / operationresults | × | × |
> | locations / operations | × | × |
> | locations / workflows | × | × |
> | operations | × | × |
> | storagesyncservices | ○ | ○ |
> | storagesyncservices / registeredservers | × | × |
> | storagesyncservices / syncgroups | × | × |
> | storagesyncservices / syncgroups / cloudendpoints | × | × |
> | storagesyncservices / syncgroups / serverendpoints | × | × |
> | storagesyncservices / workflows | × | × |

## <a name="microsoftstoragesyncdev"></a>Microsoft.StorageSyncDev

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | storagesyncservices | × | × |

## <a name="microsoftstoragesyncint"></a>Microsoft.StorageSyncInt

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | storagesyncservices | × | × |

## <a name="microsoftstorsimple"></a>Microsoft.StorSimple

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | managers | × | × |
> | operations | × | × |

## <a name="microsoftstreamanalytics"></a>Microsoft.StreamAnalytics

> [!IMPORTANT]
> 実行中状態の Stream Analytics ジョブは移動できません。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | clusters | × | × |
> | locations | × | × |
> | locations / quotas | × | × |
> | operations | × | × |
> | streamingjobs | ○ | ○ |

## <a name="microsoftstreamanalyticsexplorer"></a>Microsoft.StreamAnalyticsExplorer

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | 環境 | × | × |
> | environments/eventsources | × | × |
> | instances | × | × |
> | instances/environments | × | × |
> | instances/environments/eventsources | × | × |

## <a name="microsoftsubscription"></a>Microsoft.Subscription

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | cancel | × | × |
> | createsubscription | × | × |
> | 有効化 (enable) | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | rename | × | × |
> | subscriptiondefinitions | × | × |
> | subscriptionoperations | × | × |
> | subscriptions | × | × |

## <a name="microsoftsupport"></a>microsoft.support

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | operationresults | × | × |
> | operations | × | × |
> | operationsstatus | × | × |
> | services | × | × |
> | services / problemclassifications | × | × |
> | supporttickets | × | × |

## <a name="microsoftsynapse"></a>Microsoft.Synapse

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | checknameavailability | × | × |
> | operations | × | × |
> | workspaces | ○ | ○ |
> | workspaces / bigdatapools | ○ | ○ |
> | workspaces / operationresults | × | × |
> | workspaces / operationstatuses | × | × |
> | workspaces / sqlpools | ○ | ○ |

## <a name="microsofttimeseriesinsights"></a>Microsoft.TimeSeriesInsights

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | 環境 | ○ | ○ |
> | environments / accesspolicies | × | × |
> | environments/eventsources | ○ | ○ |
> | environments/referencedatasets | ○ | ○ |
> | operations | × | × |

## <a name="microsofttoken"></a>Microsoft.Token

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | stores | ○ | ○ |
> | stores / accesspolicies | × | × |
> | stores / services | × | × |
> | stores / services / tokens | × | × |

## <a name="microsoftvirtualmachineimages"></a>Microsoft.VirtualMachineImages

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | imagetemplates | × | × |
> | imagetemplates / runoutputs | × | × |
> | locations | × | × |
> | locations / operations | × | × |
> | operations | × | × |

## <a name="microsoftvisualstudio"></a>microsoft.visualstudio

> [!IMPORTANT]
> Azure DevOps のサブスクリプションを変更するには、[change the Azure subscription used for billing (課金に使用される Azure サブスクリプションの変更)](/azure/devops/organizations/billing/change-azure-subscription?toc=/azure/azure-resource-manager/toc.json) に関する記事をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | account | × | × |
> | account / extension | × | × |
> | account/project | × | × |
> | checknameavailability | × | × |
> | operations | × | × |

## <a name="microsoftvmware"></a>Microsoft.VMware

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | arczones | × | × |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | resourcepools | × | × |
> | vcenters | × | × |
> | virtualmachines | × | × |
> | virtualmachinetemplates | × | × |
> | virtualnetworks | × | × |

## <a name="microsoftvmwarecloudsimple"></a>Microsoft.VMwareCloudSimple

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | dedicatedcloudnodes | × | × |
> | dedicatedcloudservices | × | × |
> | locations | × | × |
> | locations / availabilities | × | × |
> | locations / operationresults | × | × |
> | locations / privateclouds | × | × |
> | locations / privateclouds / resourcepools | × | × |
> | locations / privateclouds / virtualmachinetemplates | × | × |
> | locations / privateclouds / virtualnetworks | × | × |
> | locations / usages | × | × |
> | operations | × | × |
> | virtualmachines | × | × |

## <a name="microsoftvnfmanager"></a>Microsoft.VnfManager

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | devices | × | × |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | vnfs | × | × |

## <a name="microsoftvsonline"></a>Microsoft.VSOnline

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | accounts | × | × |
> | operations | × | × |
> | plans | × | × |
> | registeredsubscriptions | × | × |

## <a name="microsoftweb"></a>Microsoft.Web

> [!IMPORTANT]
> [App Service move guidance (App Service の移動のガイダンス)](./move-limitations/app-service-move-limitations.md) に関する記事をご覧ください。

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | availablestacks | × | × |
> | billingmeters | × | × |
> | certificates | × | [○] |
> | checknameavailability | × | × |
> | connectiongateways | ○ | ○ |
> | connections | ○ | ○ |
> | customapis | ○ | ○ |
> | deletedsites | × | × |
> | deploymentlocations | × | × |
> | georegions | × | × |
> | hostingenvironments | × | × |
> | hostingenvironments / eventgridfilters | × | × |
> | hostingenvironments / multirolepools | × | × |
> | hostingenvironments / workerpools | × | × |
> | ishostingenvironmentnameavailable | × | × |
> | ishostnameavailable | × | × |
> | isusernameavailable | × | × |
> | kubeenvironments | ○ | ○ |
> | listsitesassignedtohostname | × | × |
> | locations | × | × |
> | locations / apioperations | × | × |
> | locations / connectiongatewayinstallations | × | × |
> | locations / deletedsites | × | × |
> | locations / deletevirtualnetworkorsubnets | × | × |
> | locations / extractapidefinitionfromwsdl | × | × |
> | locations / getnetworkpolicies | × | × |
> | locations / listwsdlinterfaces | × | × |
> | locations / managedapis | × | × |
> | locations / operationresults | × | × |
> | locations / operations | × | × |
> | locations / runtimes | × | × |
> | operations | × | × |
> | publishingusers | × | × |
> | recommendations | × | × |
> | resourcehealthmetadata | × | × |
> | runtimes | × | × |
> | serverfarms | ○ | ○ |
> | serverfarms / eventgridfilters | × | × |
> | sites | ○ | ○ |
> | sites / eventgridfilters | × | × |
> | sites / hostnamebindings | × | × |
> | sites / networkconfig | × | × |
> | sites/premieraddons | ○ | ○ |
> | sites/slots | ○ | ○ |
> | sites / slots / eventgridfilters | × | × |
> | sites / slots / hostnamebindings | × | × |
> | sites / slots / networkconfig | × | × |
> | sourcecontrols | × | × |
> | staticsites | × | × |
> | validate | × | × |
> | verifyhostingenvironmentvnet | × | × |

## <a name="microsoftwindowsesu"></a>Microsoft.WindowsESU

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | multipleactivationkeys | × | × |
> | operations | × | × |

## <a name="microsoftwindowsiot"></a>Microsoft.WindowsIoT

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | deviceservices | × | × |
> | operations | × | × |

## <a name="microsoftworkloadbuilder"></a>Microsoft.WorkloadBuilder

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | locations | × | × |
> | locations / operationstatuses | × | × |
> | operations | × | × |
> | workloads | × | × |

## <a name="microsoftworkloadmonitor"></a>Microsoft.WorkloadMonitor

> [!div class="mx-tableFixed"]
> | リソースの種類 | Resource group | サブスクリプション |
> | ------------- | ----------- | ---------- |
> | components | × | × |
> | componentssummary | × | × |
> | monitorinstances | × | × |
> | monitorinstancessummary | × | × |
> | monitors | × | × |
> | notificationsettings | × | × |
> | operations | × | × |

## <a name="third-party-services"></a>サード パーティーのサービス

サード パーティのサービスは現在、移動操作をサポートしていません。

## <a name="next-steps"></a>次のステップ
リソースの移動のコマンドについては、「[新しいリソース グループまたはサブスクリプションへのリソースの移動](move-resource-group-and-subscription.md)」を参照してください。

コンマ区切りの値のファイルと同じデータを取得するには、[move-support-resources.csv](https://github.com/tfitzmac/resource-capabilities/blob/master/move-support-resources.csv) をダウンロードします。
