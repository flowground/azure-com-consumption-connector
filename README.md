# ![LOGO](logo.png) ConsumptionManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the ConsumptionManagementClient API (version 2019-01-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/consumption/2019-01-01/swagger.json<br/>
Generated at: 2019-05-07T17:37:51+03:00

## API Description

Consumption management client provides access to consumption resources for Azure Enterprise Subscriptions.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Gets the balances for a scope by billing period and billingAccountId. Balances are available via this API only for May 1, 2014 or later.

*Tags:* `Balances`

#### Input Parameters
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `billingAccountId` - _required_ - BillingAccount ID
* `billingPeriodName` - _required_ - Billing Period Name.

### Gets the balances for a scope by billingAccountId. Balances are available via this API only for May 1, 2014 or later.

*Tags:* `Balances`

#### Input Parameters
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `billingAccountId` - _required_ - BillingAccount ID

### Lists the reservations details for provided date range.

*Tags:* `ReservedInstances`

#### Input Parameters
* `reservationOrderId` - _required_ - Order Id of the reservation
* `$filter` - _required_ - Filter reservation details by date range. The properties/UsageDate for start date and end date. The filter supports 'le' and  'ge' 
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Lists the reservations summaries for daily or monthly grain.

*Tags:* `ReservedInstances`

#### Input Parameters
* `reservationOrderId` - _required_ - Order Id of the reservation
* `grain` - _required_ - Can be daily or monthly
    Possible values: daily, monthly.
* `$filter` - _optional_ - Required only for daily grain. The properties/UsageDate for start date and end date. The filter supports 'le' and  'ge'
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Lists the reservations details for provided date range.

*Tags:* `ReservedInstances`

#### Input Parameters
* `reservationOrderId` - _required_ - Order Id of the reservation
* `reservationId` - _required_ - Id of the reservation
* `$filter` - _required_ - Filter reservation details by date range. The properties/UsageDate for start date and end date. The filter supports 'le' and  'ge' 
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Lists the reservations summaries for daily or monthly grain.

*Tags:* `ReservedInstances`

#### Input Parameters
* `reservationOrderId` - _required_ - Order Id of the reservation
* `reservationId` - _required_ - Id of the reservation
* `grain` - _required_ - Can be daily or monthly
    Possible values: daily, monthly.
* `$filter` - _optional_ - Required only for daily grain. The properties/UsageDate for start date and end date. The filter supports 'le' and  'ge'
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Lists all of the available consumption REST API operations.

*Tags:* `Operations`

#### Input Parameters
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Provides the aggregate cost of a management group and all child management groups by specified billing period

*Tags:* `AggregatedCost`

#### Input Parameters
* `managementGroupId` - _required_ - Azure Management Group ID.
* `billingPeriodName` - _required_ - Billing Period Name.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Provides the aggregate cost of a management group and all child management groups by current billing period.

*Tags:* `AggregatedCost`

#### Input Parameters
* `managementGroupId` - _required_ - Azure Management Group ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `$filter` - _optional_ - May be used to filter aggregated cost by properties/usageStart (Utc time), properties/usageEnd (Utc time). The filter supports 'eq', 'lt', 'gt', 'le', 'ge', and 'and'. It does not currently support 'ne', 'or', or 'not'. Tag filter is a key value pair string where key and value is separated by a colon (:).

### Get the price sheet for a scope by subscriptionId and billing period. Price sheet is available via this API only for May 1, 2014 or later.

*Tags:* `PriceSheet`

#### Input Parameters
* `$expand` - _optional_ - May be used to expand the properties/meterDetails within a price sheet. By default, these fields are not included when returning price sheet.
* `$skiptoken` - _optional_ - Skiptoken is only used if a previous operation returned a partial result. If a previous response contains a nextLink element, the value of the nextLink element will include a skiptoken parameter that specifies a starting point to use for subsequent calls.
* `$top` - _optional_ - May be used to limit the number of results to the top N results.
* `subscriptionId` - _required_ - Azure Subscription ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `billingPeriodName` - _required_ - Billing Period Name.

### Lists the forecast charges by subscriptionId.

*Tags:* `Forecasts`

#### Input Parameters
* `$filter` - _optional_ - May be used to filter forecasts by properties/usageDate (Utc time), properties/chargeType or properties/grain. The filter supports 'eq', 'lt', 'gt', 'le', 'ge', and 'and'. It does not currently support 'ne', 'or', or 'not'.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `subscriptionId` - _required_ - Azure Subscription ID.

### Gets the price sheet for a scope by subscriptionId. Price sheet is available via this API only for May 1, 2014 or later.

*Tags:* `PriceSheet`

#### Input Parameters
* `$expand` - _optional_ - May be used to expand the properties/meterDetails within a price sheet. By default, these fields are not included when returning price sheet.
* `$skiptoken` - _optional_ - Skiptoken is only used if a previous operation returned a partial result. If a previous response contains a nextLink element, the value of the nextLink element will include a skiptoken parameter that specifies a starting point to use for subsequent calls.
* `$top` - _optional_ - May be used to limit the number of results to the top N results.
* `subscriptionId` - _required_ - Azure Subscription ID.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### List of recommendations for purchasing reserved instances.

*Tags:* `ReservationRecommendations`

#### Input Parameters
* `$filter` - _optional_ - May be used to filter reservationRecommendations by properties/scope and properties/lookBackPeriod.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `subscriptionId` - _required_ - Azure Subscription ID.

### Lists all budgets for the defined scope.

*Tags:* `Budgets`

#### Input Parameters
* `scope` - _required_ - The scope associated with budget operations. This includes '/subscriptions/{subscriptionId}/' for subscription scope, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, '/providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### The operation to delete a budget.

*Tags:* `Budgets`

#### Input Parameters
* `scope` - _required_ - The scope associated with budget operations. This includes '/subscriptions/{subscriptionId}/' for subscription scope, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, '/providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `budgetName` - _required_ - Budget Name.

### Gets the budget for the scope by budget name.

*Tags:* `Budgets`

#### Input Parameters
* `scope` - _required_ - The scope associated with budget operations. This includes '/subscriptions/{subscriptionId}/' for subscription scope, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, '/providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `budgetName` - _required_ - Budget Name.

### The operation to create or update a budget. Update operation requires latest eTag to be set in the request mandatorily. You may obtain the latest eTag by performing a get operation. Create operation does not require eTag.

*Tags:* `Budgets`

#### Input Parameters
* `scope` - _required_ - The scope associated with budget operations. This includes '/subscriptions/{subscriptionId}/' for subscription scope, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, '/providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope.
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `budgetName` - _required_ - Budget Name.

### Lists the charges based for the defined scope.

*Tags:* `Charges`

#### Input Parameters
* `scope` - _required_ - The scope associated with usage details operations. This includes '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope and '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope. For department and enrollment accounts, you can also add billing period to the scope using '/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}'. For e.g. to specify billing period at department scope use '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}'
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.
* `$filter` - _optional_ - May be used to filter charges by properties/usageEnd (Utc time), properties/usageStart (Utc time). The filter supports 'eq', 'lt', 'gt', 'le', 'ge', and 'and'. It does not currently support 'ne', 'or', or 'not'. Tag filter is a key value pair string where key and value is separated by a colon (:).

### Lists the marketplaces for a scope at the defined scope. Marketplaces are available via this API only for May 1, 2014 or later.

*Tags:* `Marketplaces`

#### Input Parameters
* `$filter` - _optional_ - May be used to filter marketplaces by properties/usageEnd (Utc time), properties/usageStart (Utc time), properties/resourceGroup, properties/instanceName or properties/instanceId. The filter supports 'eq', 'lt', 'gt', 'le', 'ge', and 'and'. It does not currently support 'ne', 'or', or 'not'.
* `$top` - _optional_ - May be used to limit the number of results to the most recent N marketplaces.
* `$skiptoken` - _optional_ - Skiptoken is only used if a previous operation returned a partial result. If a previous response contains a nextLink element, the value of the nextLink element will include a skiptoken parameter that specifies a starting point to use for subsequent calls.
* `scope` - _required_ - The scope associated with marketplace operations. This includes '/subscriptions/{subscriptionId}/' for subscription scope, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, '/providers/Microsoft.Billing/departments/{departmentId}' for Department scope, '/providers/Microsoft.Billing/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope and '/providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope. For subscription, billing account, department, enrollment account and ManagementGroup, you can also add billing period to the scope using '/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}'. For e.g. to specify billing period at department scope use '/providers/Microsoft.Billing/departments/{departmentId}/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}'
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Get all available tag keys for the defined scope

*Tags:* `Tags`

#### Input Parameters
* `scope` - _required_ - The scope associated with tags operations. This includes '/subscriptions/{subscriptionId}/' for subscription scope, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope and '/providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope..
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

### Lists the usage details for the defined scope. Usage details are available via this API only for May 1, 2014 or later.

*Tags:* `UsageDetails`

#### Input Parameters
* `scope` - _required_ - The scope associated with usage details operations. This includes '/subscriptions/{subscriptionId}/' for subscription scope, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, '/providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, '/providers/Microsoft.Billing/departments/{departmentId}' for Department scope, '/providers/Microsoft.Billing/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope and '/providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope. For subscription, billing account, department, enrollment account and management group, you can also add billing period to the scope using '/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}'. For e.g. to specify billing period at department scope use '/providers/Microsoft.Billing/departments/{departmentId}/providers/Microsoft.Billing/billingPeriods/{billingPeriodName}'
* `$expand` - _optional_ - May be used to expand the properties/additionalProperties or properties/meterDetails within a list of usage details. By default, these fields are not included when listing usage details.
* `$filter` - _optional_ - May be used to filter usageDetails by properties/usageEnd (Utc time), properties/usageStart (Utc time), properties/resourceGroup, properties/instanceName, properties/instanceId or tags. The filter supports 'eq', 'lt', 'gt', 'le', 'ge', and 'and'. It does not currently support 'ne', 'or', or 'not'. Tag filter is a key value pair string where key and value is separated by a colon (:).
* `$skiptoken` - _optional_ - Skiptoken is only used if a previous operation returned a partial result. If a previous response contains a nextLink element, the value of the nextLink element will include a skiptoken parameter that specifies a starting point to use for subsequent calls.
* `$top` - _optional_ - May be used to limit the number of results to the most recent N usageDetails.
* `$apply` - _optional_ - OData apply expression to aggregate usageDetails by tags or (tags and properties/usageStart)
* `api-version` - _required_ - Version of the API to be used with the client request. The current version is 2019-01-01.

## License

**flow**ground :- Telekom iPaaS / azure-com-consumption-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
