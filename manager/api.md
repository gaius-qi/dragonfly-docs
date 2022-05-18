# Dragonfly Manager


<a name="overview"></a>
## Overview
Dragonfly Manager Server


### Version information
*Version* : 1.0.0


### License information
*License* : Apache 2.0  
*Terms of service* : null


### URI scheme
*Host* : localhost:8080  
*BasePath* : /api/v1




<a name="paths"></a>
## Paths

<a name="api-v1-applications-post"></a>
### Create Application
```
POST /api/v1/applications
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**Application**  <br>*required*|Application|[types.CreateApplicationRequest](#types-createapplicationrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Application](#model-application)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-get"></a>
### Get Applications
```
GET /api/v1/applications
```


#### Description
Get Applications


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.Application](#model-application) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-id-get"></a>
### Get Application
```
GET /api/v1/applications/{id}
```


#### Description
Get Application by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Application](#model-application)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-id-delete"></a>
### Destroy Application
```
DELETE /api/v1/applications/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-id-patch"></a>
### Update Application
```
PATCH /api/v1/applications/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**Application**  <br>*required*|Application|[types.UpdateApplicationRequest](#types-updateapplicationrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Application](#model-application)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-id-scheduler-clusters-scheduler_cluster_id-put"></a>
### Add Scheduler to Application
```
PUT /api/v1/applications/{id}/scheduler-clusters/{scheduler_cluster_id}
```


#### Description
Add Scheduler to Application


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**scheduler_cluster_id**  <br>*required*|scheduler cluster id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-id-scheduler-clusters-scheduler_cluster_id-delete"></a>
### Delete Scheduler to Application
```
DELETE /api/v1/applications/{id}/scheduler-clusters/{scheduler_cluster_id}
```


#### Description
Delete Scheduler to Application


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**scheduler_cluster_id**  <br>*required*|scheduler cluster id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-id-seed-peer-clusters-seed_peer_cluster_id-put"></a>
### Add SeedPeer to Application
```
PUT /api/v1/applications/{id}/seed-peer-clusters/{seed_peer_cluster_id}
```


#### Description
Add SeedPeer to Application


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**seed_peer_cluster_id**  <br>*required*|seed peer cluster id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-applications-id-seed-peer-clusters-seed_peer_cluster_id-delete"></a>
### Delete SeedPeer to Application
```
DELETE /api/v1/applications/{id}/seed-peer-clusters/{seed_peer_cluster_id}
```


#### Description
Delete SeedPeer to Application


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**seed_peer_cluster_id**  <br>*required*|seed peer cluster id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Application


<a name="api-v1-configs-post"></a>
### Create Config
```
POST /api/v1/configs
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**Config**  <br>*required*|Config|[types.CreateConfigRequest](#types-createconfigrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Config](#model-config)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Config


<a name="api-v1-configs-get"></a>
### Get Configs
```
GET /api/v1/configs
```


#### Description
Get Configs


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.Config](#model-config) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Config


<a name="api-v1-configs-id-get"></a>
### Get Config
```
GET /api/v1/configs/{id}
```


#### Description
Get Config by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Config](#model-config)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Config


<a name="api-v1-configs-id-delete"></a>
### Destroy Config
```
DELETE /api/v1/configs/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Config


<a name="api-v1-configs-id-patch"></a>
### Update Config
```
PATCH /api/v1/configs/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**Config**  <br>*required*|Config|[types.UpdateConfigRequest](#types-updateconfigrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Config](#model-config)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Config


<a name="api-v1-healthy-get"></a>
### Get Health
```
GET /api/v1/healthy
```


#### Description
Get app health


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Health


<a name="api-v1-jobs-post"></a>
### Create Job
```
POST /api/v1/jobs
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**Job**  <br>*required*|Job|[types.CreateJobRequest](#types-createjobrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Job](#model-job)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Job


<a name="api-v1-jobs-get"></a>
### Get Jobs
```
GET /api/v1/jobs
```


#### Description
Get Jobs


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.Job](#model-job) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Job


<a name="api-v1-jobs-id-get"></a>
### Get Job
```
GET /api/v1/jobs/{id}
```


#### Description
Get Job by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Job](#model-job)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Job


<a name="api-v1-jobs-id-delete"></a>
### Destroy Job
```
DELETE /api/v1/jobs/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Job


<a name="api-v1-jobs-id-patch"></a>
### Update Job
```
PATCH /api/v1/jobs/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**Job**  <br>*required*|Job|[types.UpdateJobRequest](#types-updatejobrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Job](#model-job)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Job


<a name="api-v1-oauth-post"></a>
### Create Oauth
```
POST /api/v1/oauth
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**Oauth**  <br>*required*|Oauth|[types.CreateOauthRequest](#types-createoauthrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Oauth](#model-oauth)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Oauth


<a name="api-v1-oauth-get"></a>
### Get Oauths
```
GET /api/v1/oauth
```


#### Description
Get Oauths


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.Oauth](#model-oauth) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Oauth


<a name="api-v1-oauth-id-get"></a>
### Get Oauth
```
GET /api/v1/oauth/{id}
```


#### Description
Get Oauth by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Oauth](#model-oauth)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Oauth


<a name="api-v1-oauth-id-delete"></a>
### Destroy Oauth
```
DELETE /api/v1/oauth/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Oauth


<a name="api-v1-oauth-id-patch"></a>
### Update Oauth
```
PATCH /api/v1/oauth/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**Oauth**  <br>*required*|Oauth|[types.UpdateOauthRequest](#types-updateoauthrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Oauth](#model-oauth)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Oauth


<a name="api-v1-permissions-get"></a>
### Get Permissions
```
GET /api/v1/permissions
```


#### Description
Get Permissions


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [rbac.Permission](#rbac-permission) > array|
|**400**||No Content|
|**500**||No Content|


#### Produces

* `application/json`


#### Tags

* Permission


<a name="api-v1-preheats-post"></a>
### Create V1 Preheat
```
POST /api/v1/preheats
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**Preheat**  <br>*required*|Preheat|[types.CreateV1PreheatRequest](#types-createv1preheatrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[types.CreateV1PreheatResponse](#types-createv1preheatresponse)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Preheat


<a name="api-v1-preheats-id-get"></a>
### Get V1 Preheat
```
GET /api/v1/preheats/{id}
```


#### Description
Get Preheat by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[types.GetV1PreheatResponse](#types-getv1preheatresponse)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Preheat


<a name="api-v1-roles-post"></a>
### Create Role
```
POST /api/v1/roles
```


#### Description
Create Role by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**Role**  <br>*required*|Role|[types.CreateRoleRequest](#types-createrolerequest)|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Role


<a name="api-v1-roles-get"></a>
### Get Roles
```
GET /api/v1/roles
```


#### Description
Get roles


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Role


<a name="api-v1-roles-role-get"></a>
### Get Role
```
GET /api/v1/roles/:role
```


#### Description
Get Role


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**role**  <br>*required*|role|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Role


<a name="api-v1-roles-role-delete"></a>
### Destroy Role
```
DELETE /api/v1/roles/:role
```


#### Description
Destroy role by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**role**  <br>*required*|role|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Role


<a name="api-v1-roles-role-permissions-post"></a>
### Add Permission For Role
```
POST /api/v1/roles/:role/permissions
```


#### Description
Add Permission by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**role**  <br>*required*|role|string|
|**Body**|**Permission**  <br>*required*|Permission|[types.AddPermissionForRoleRequest](#types-addpermissionforrolerequest)|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Role


<a name="api-v1-roles-role-permissions-delete"></a>
### Update Role
```
DELETE /api/v1/roles/:role/permissions
```


#### Description
Remove Role Permission by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**role**  <br>*required*|role|string|
|**Body**|**Permission**  <br>*required*|Permission|[types.DeletePermissionForRoleRequest](#types-deletepermissionforrolerequest)|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Role


<a name="api-v1-scheduler-clusters-post"></a>
### Create SchedulerCluster
```
POST /api/v1/scheduler-clusters
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**SchedulerCluster**  <br>*required*|SchedulerCluster|[types.CreateSchedulerClusterRequest](#types-createschedulerclusterrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SchedulerCluster](#model-schedulercluster)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SchedulerCluster


<a name="api-v1-scheduler-clusters-get"></a>
### Get SchedulerClusters
```
GET /api/v1/scheduler-clusters
```


#### Description
Get SchedulerClusters


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.SchedulerCluster](#model-schedulercluster) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SchedulerCluster


<a name="api-v1-scheduler-clusters-id-get"></a>
### Get SchedulerCluster
```
GET /api/v1/scheduler-clusters/{id}
```


#### Description
Get SchedulerCluster by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SchedulerCluster](#model-schedulercluster)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SchedulerCluster


<a name="api-v1-scheduler-clusters-id-delete"></a>
### Destroy SchedulerCluster
```
DELETE /api/v1/scheduler-clusters/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SchedulerCluster


<a name="api-v1-scheduler-clusters-id-patch"></a>
### Update SchedulerCluster
```
PATCH /api/v1/scheduler-clusters/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**SchedulerCluster**  <br>*required*|SchedulerCluster|[types.UpdateSchedulerClusterRequest](#types-updateschedulerclusterrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SchedulerCluster](#model-schedulercluster)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SchedulerCluster


<a name="api-v1-scheduler-clusters-id-schedulers-scheduler_id-put"></a>
### Add Scheduler to schedulerCluster
```
PUT /api/v1/scheduler-clusters/{id}/schedulers/{scheduler_id}
```


#### Description
Add Scheduler to schedulerCluster


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**scheduler_id**  <br>*required*|scheduler id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SchedulerCluster


<a name="api-v1-schedulers-post"></a>
### Create Scheduler
```
POST /api/v1/schedulers
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**Scheduler**  <br>*required*|Scheduler|[types.CreateSchedulerRequest](#types-createschedulerrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Scheduler](#model-scheduler)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Scheduler


<a name="api-v1-schedulers-get"></a>
### Get Schedulers
```
GET /api/v1/schedulers
```


#### Description
Get Schedulers


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.Scheduler](#model-scheduler) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Scheduler


<a name="api-v1-schedulers-id-get"></a>
### Get Scheduler
```
GET /api/v1/schedulers/{id}
```


#### Description
Get Scheduler by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Scheduler](#model-scheduler)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Scheduler


<a name="api-v1-schedulers-id-delete"></a>
### Destroy Scheduler
```
DELETE /api/v1/schedulers/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Scheduler


<a name="api-v1-schedulers-id-patch"></a>
### Update Scheduler
```
PATCH /api/v1/schedulers/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**Scheduler**  <br>*required*|Scheduler|[types.UpdateSchedulerRequest](#types-updateschedulerrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.Scheduler](#model-scheduler)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Scheduler


<a name="api-v1-security-groups-post"></a>
### Create SecurityGroup
```
POST /api/v1/security-groups
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**SecurityGroup**  <br>*required*|SecurityGroup|[types.CreateSecurityGroupRequest](#types-createsecuritygrouprequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SecurityGroup](#model-securitygroup)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-groups-get"></a>
### Get SecurityGroups
```
GET /api/v1/security-groups
```


#### Description
Get SecurityGroups


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.SecurityGroup](#model-securitygroup) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-groups-id-get"></a>
### Get SecurityGroup
```
GET /api/v1/security-groups/{id}
```


#### Description
Get SecurityGroup by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SecurityGroup](#model-securitygroup)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-groups-id-patch"></a>
### Update SecurityGroup
```
PATCH /api/v1/security-groups/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**SecurityGroup**  <br>*required*|SecurityGroup|[types.UpdateSecurityGroupRequest](#types-updatesecuritygrouprequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SecurityGroup](#model-securitygroup)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-groups-id-scheduler-clusters-scheduler_cluster_id-put"></a>
### Add Scheduler to SecurityGroup
```
PUT /api/v1/security-groups/{id}/scheduler-clusters/{scheduler_cluster_id}
```


#### Description
Add Scheduler to SecurityGroup


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**scheduler_cluster_id**  <br>*required*|scheduler cluster id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-groups-id-security-rules-security_rule_id-put"></a>
### Add SecurityRule to SecurityGroup
```
PUT /api/v1/security-groups/{id}/security-rules/{security_rule_id}
```


#### Description
Add SecurityRule to SecurityGroup


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**security_rule_id**  <br>*required*|security rule id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-groups-id-security-rules-security_rule_id-delete"></a>
### Destroy SecurityRule to SecurityGroup
```
DELETE /api/v1/security-groups/{id}/security-rules/{security_rule_id}
```


#### Description
Destroy SecurityRule to SecurityGroup


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**security_rule_id**  <br>*required*|security rule id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-groups-id-seed-peer-clusters-seed_peer_cluster_id-put"></a>
### Add SeedPeer to SecurityGroup
```
PUT /api/v1/security-groups/{id}/seed-peer-clusters/{seed_peer_cluster_id}
```


#### Description
Add SeedPeer to SecurityGroup


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**seed_peer_cluster_id**  <br>*required*|seed peer cluster id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-security-rules-post"></a>
### Create SecurityRule
```
POST /api/v1/security-rules
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**SecurityRule**  <br>*required*|SecurityRule|[types.CreateSecurityRuleRequest](#types-createsecurityrulerequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SecurityRule](#model-securityrule)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityRule


<a name="api-v1-security-rules-get"></a>
### Get SecurityRules
```
GET /api/v1/security-rules
```


#### Description
Get SecurityRules


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.SecurityRule](#model-securityrule) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityRule


<a name="api-v1-security-rules-id-get"></a>
### Get SecurityRule
```
GET /api/v1/security-rules/{id}
```


#### Description
Get SecurityRule by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SecurityRule](#model-securityrule)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityRule


<a name="api-v1-security-rules-id-patch"></a>
### Update SecurityRule
```
PATCH /api/v1/security-rules/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**SecurityRule**  <br>*required*|SecurityRule|[types.UpdateSecurityRuleRequest](#types-updatesecurityrulerequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SecurityRule](#model-securityrule)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityRule


<a name="api-v1-securitygroups-id-delete"></a>
### Destroy SecurityGroup
```
DELETE /api/v1/securityGroups/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityGroup


<a name="api-v1-securityrules-id-delete"></a>
### Destroy SecurityRule
```
DELETE /api/v1/securityRules/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SecurityRule


<a name="api-v1-seed-peer-clusters-post"></a>
### Create SeedPeerCluster
```
POST /api/v1/seed-peer-clusters
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**SeedPeerCluster**  <br>*required*|DNCluster|[types.CreateSeedPeerClusterRequest](#types-createseedpeerclusterrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SeedPeerCluster](#model-seedpeercluster)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeerCluster


<a name="api-v1-seed-peer-clusters-get"></a>
### Get SeedPeerClusters
```
GET /api/v1/seed-peer-clusters
```


#### Description
Get SeedPeerClusters


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.SeedPeerCluster](#model-seedpeercluster) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeerCluster


<a name="api-v1-seed-peer-clusters-id-get"></a>
### Get SeedPeerCluster
```
GET /api/v1/seed-peer-clusters/{id}
```


#### Description
Get SeedPeerCluster by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SeedPeerCluster](#model-seedpeercluster)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeerCluster


<a name="api-v1-seed-peer-clusters-id-delete"></a>
### Destroy SeedPeerCluster
```
DELETE /api/v1/seed-peer-clusters/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeerCluster


<a name="api-v1-seed-peer-clusters-id-patch"></a>
### Update SeedPeerCluster
```
PATCH /api/v1/seed-peer-clusters/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**SeedPeerCluster**  <br>*required*|SeedPeerCluster|[types.UpdateSeedPeerClusterRequest](#types-updateseedpeerclusterrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SeedPeerCluster](#model-seedpeercluster)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeerCluster


<a name="api-v1-seed-peer-clusters-id-scheduler-clusters-scheduler_cluster_id-put"></a>
### Add SchedulerCluster to SeedPeerCluster
```
PUT /api/v1/seed-peer-clusters/{id}/scheduler-clusters/{scheduler_cluster_id}
```


#### Description
Add SchedulerCluster to SeedPeerCluster


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**scheduler_cluster_id**  <br>*required*|scheduler cluster id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeerCluster


<a name="api-v1-seed-peer-clusters-id-seed-peers-seed_peer_id-put"></a>
### Add Instance to SeedPeerCluster
```
PUT /api/v1/seed-peer-clusters/{id}/seed-peers/{seed_peer_id}
```


#### Description
Add SeedPeer to SeedPeerCluster


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**seed_peer_id**  <br>*required*|seed peer id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeerCluster


<a name="api-v1-seed-peers-post"></a>
### Create SeedPeer
```
POST /api/v1/seed-peers
```


#### Description
create by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**SeedPeer**  <br>*required*|SeedPeer|[types.CreateSeedPeerRequest](#types-createseedpeerrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SeedPeer](#model-seedpeer)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeer


<a name="api-v1-seed-peers-get"></a>
### Get SeedPeers
```
GET /api/v1/seed-peers
```


#### Description
Get SeedPeers


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.SeedPeer](#model-seedpeer) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeer


<a name="api-v1-seed-peers-id-get"></a>
### Get SeedPeer
```
GET /api/v1/seed-peers/{id}
```


#### Description
Get SeedPeer by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SeedPeer](#model-seedpeer)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeer


<a name="api-v1-seed-peers-id-delete"></a>
### Destroy SeedPeer
```
DELETE /api/v1/seed-peers/{id}
```


#### Description
Destroy by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeer


<a name="api-v1-seed-peers-id-patch"></a>
### Update SeedPeer
```
PATCH /api/v1/seed-peers/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**SeedPeer**  <br>*required*|SeedPeer|[types.UpdateSeedPeerRequest](#types-updateseedpeerrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.SeedPeer](#model-seedpeer)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* SeedPeer


<a name="api-v1-user-signin-name-get"></a>
### Oauth Signin
```
GET /api/v1/user/signin/{name}
```


#### Description
oauth signin by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**name**  <br>*required*|name|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* User


<a name="api-v1-user-signin-name-callback-get"></a>
### Oauth Signin Callback
```
GET /api/v1/user/signin/{name}/callback
```


#### Description
oauth signin callback by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**name**  <br>*required*|name|string|
|**Query**|**code**  <br>*required*|code|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**404**|No Content|
|**500**|No Content|


#### Tags

* Oauth


<a name="api-v1-user-signup-post"></a>
### SignUp user
```
POST /api/v1/user/signup
```


#### Description
signup by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**User**  <br>*required*|User|[types.SignUpRequest](#types-signuprequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.User](#model-user)|
|**400**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* User


<a name="api-v1-users-get"></a>
### Get Users
```
GET /api/v1/users
```


#### Description
Get Users


#### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Query**|**page**  <br>*required*|current page|integer|`0`|
|**Query**|**per_page**  <br>*required*|return max item count, default 10, max 50|integer|`10`|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< [model.User](#model-user) > array|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* User


<a name="api-v1-users-id-get"></a>
### Get User
```
GET /api/v1/users/{id}
```


#### Description
Get User by id


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.User](#model-user)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* User


<a name="api-v1-users-id-patch"></a>
### Update User
```
PATCH /api/v1/users/{id}
```


#### Description
Update by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Body**|**User**  <br>*required*|User|[types.UpdateUserRequest](#types-updateuserrequest)|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|[model.User](#model-user)|
|**400**||No Content|
|**404**||No Content|
|**500**||No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* User


<a name="api-v1-users-id-reset_password-post"></a>
### Reset Password For User
```
POST /api/v1/users/{id}/reset_password
```


#### Description
reset password by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Body**|**User**  <br>*required*|User|[types.ResetPasswordRequest](#types-resetpasswordrequest)|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* User


<a name="api-v1-users-id-roles-get"></a>
### Get User Roles
```
GET /api/v1/users/{id}/roles
```


#### Description
get roles by json config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|


#### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|OK|< string > array|
|**400**||No Content|
|**500**||No Content|


#### Produces

* `application/json`


#### Tags

* User


<a name="api-v1-users-id-roles-role-put"></a>
### Add Role For User
```
PUT /api/v1/users/{id}/roles/{role}
```


#### Description
add role to user by uri config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**role**  <br>*required*|role|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Users


<a name="api-v1-users-id-roles-role-delete"></a>
### Delete Role For User
```
DELETE /api/v1/users/{id}/roles/{role}
```


#### Description
delete role by uri config


#### Parameters

|Type|Name|Description|Schema|
|---|---|---|---|
|**Path**|**id**  <br>*required*|id|string|
|**Path**|**role**  <br>*required*|role|string|


#### Responses

|HTTP Code|Schema|
|---|---|
|**200**|No Content|
|**400**|No Content|
|**500**|No Content|


#### Consumes

* `application/json`


#### Produces

* `application/json`


#### Tags

* Users




<a name="definitions"></a>
## Definitions

<a name="model-application"></a>
### model.Application

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**created_at**  <br>*optional*|string|
|**download_rate_limit**  <br>*optional*|integer|
|**id**  <br>*optional*|integer|
|**name**  <br>*optional*|string|
|**scheduler_clusters**  <br>*optional*|< [model.SchedulerCluster](#model-schedulercluster) > array|
|**seed_peer_clusters**  <br>*optional*|< [model.SeedPeerCluster](#model-seedpeercluster) > array|
|**state**  <br>*optional*|string|
|**updated_at**  <br>*optional*|string|
|**url**  <br>*optional*|string|
|**user**  <br>*optional*|[model.User](#model-user)|
|**user_id**  <br>*optional*|integer|


<a name="model-config"></a>
### model.Config

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**created_at**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**name**  <br>*optional*|string|
|**updated_at**  <br>*optional*|string|
|**user_id**  <br>*optional*|integer|
|**value**  <br>*optional*|string|


<a name="model-jsonmap"></a>
### model.JSONMap
*Type* : object


<a name="model-job"></a>
### model.Job

|Name|Schema|
|---|---|
|**args**  <br>*optional*|[model.JSONMap](#model-jsonmap)|
|**bio**  <br>*optional*|string|
|**created_at**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**result**  <br>*optional*|[model.JSONMap](#model-jsonmap)|
|**scheduler_clusters**  <br>*optional*|< [model.SchedulerCluster](#model-schedulercluster) > array|
|**seed_peer_clusters**  <br>*optional*|< [model.SeedPeerCluster](#model-seedpeercluster) > array|
|**state**  <br>*optional*|string|
|**task_id**  <br>*optional*|string|
|**type**  <br>*optional*|string|
|**updated_at**  <br>*optional*|string|
|**user_id**  <br>*optional*|integer|


<a name="model-oauth"></a>
### model.Oauth

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**client_id**  <br>*optional*|string|
|**client_secret**  <br>*optional*|string|
|**created_at**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**name**  <br>*optional*|string|
|**redirect_url**  <br>*optional*|string|
|**updated_at**  <br>*optional*|string|


<a name="model-scheduler"></a>
### model.Scheduler

|Name|Schema|
|---|---|
|**created_at**  <br>*optional*|string|
|**host_name**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**idc**  <br>*optional*|string|
|**ip**  <br>*optional*|string|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|
|**port**  <br>*optional*|integer|
|**schedulerClusterID**  <br>*optional*|integer|
|**state**  <br>*optional*|string|
|**updated_at**  <br>*optional*|string|


<a name="model-schedulercluster"></a>
### model.SchedulerCluster

|Name|Schema|
|---|---|
|**application_id**  <br>*optional*|integer|
|**bio**  <br>*optional*|string|
|**client_config**  <br>*optional*|[model.JSONMap](#model-jsonmap)|
|**config**  <br>*optional*|[model.JSONMap](#model-jsonmap)|
|**created_at**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**is_default**  <br>*optional*|boolean|
|**jobs**  <br>*optional*|< [model.Job](#model-job) > array|
|**name**  <br>*optional*|string|
|**scopes**  <br>*optional*|[model.JSONMap](#model-jsonmap)|
|**security_group_id**  <br>*optional*|integer|
|**seed_peer_clusters**  <br>*optional*|< [model.SeedPeerCluster](#model-seedpeercluster) > array|
|**updated_at**  <br>*optional*|string|


<a name="model-securitygroup"></a>
### model.SecurityGroup

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**created_at**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**name**  <br>*optional*|string|
|**security_rules**  <br>*optional*|< [model.SecurityRule](#model-securityrule) > array|
|**updated_at**  <br>*optional*|string|


<a name="model-securityrule"></a>
### model.SecurityRule

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**created_at**  <br>*optional*|string|
|**domain**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**name**  <br>*optional*|string|
|**proxy_domain**  <br>*optional*|string|
|**security_groups**  <br>*optional*|< [model.SecurityGroup](#model-securitygroup) > array|
|**updated_at**  <br>*optional*|string|


<a name="model-seedpeer"></a>
### model.SeedPeer

|Name|Schema|
|---|---|
|**created_at**  <br>*optional*|string|
|**download_port**  <br>*optional*|integer|
|**host_name**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**idc**  <br>*optional*|string|
|**ip**  <br>*optional*|string|
|**is_cdn**  <br>*optional*|boolean|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|
|**port**  <br>*optional*|integer|
|**seedPeerClusterID**  <br>*optional*|integer|
|**state**  <br>*optional*|string|
|**type**  <br>*optional*|string|
|**updated_at**  <br>*optional*|string|


<a name="model-seedpeercluster"></a>
### model.SeedPeerCluster

|Name|Schema|
|---|---|
|**application_id**  <br>*optional*|integer|
|**bio**  <br>*optional*|string|
|**config**  <br>*optional*|[model.JSONMap](#model-jsonmap)|
|**created_at**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**is_default**  <br>*optional*|boolean|
|**jobs**  <br>*optional*|< [model.Job](#model-job) > array|
|**name**  <br>*optional*|string|
|**scheduler_clusters**  <br>*optional*|< [model.SchedulerCluster](#model-schedulercluster) > array|
|**scopes**  <br>*optional*|[model.JSONMap](#model-jsonmap)|
|**security_group_id**  <br>*optional*|integer|
|**updated_at**  <br>*optional*|string|


<a name="model-user"></a>
### model.User

|Name|Schema|
|---|---|
|**avatar**  <br>*optional*|string|
|**bio**  <br>*optional*|string|
|**created_at**  <br>*optional*|string|
|**email**  <br>*optional*|string|
|**id**  <br>*optional*|integer|
|**location**  <br>*optional*|string|
|**name**  <br>*optional*|string|
|**phone**  <br>*optional*|string|
|**state**  <br>*optional*|string|
|**updated_at**  <br>*optional*|string|


<a name="rbac-permission"></a>
### rbac.Permission

|Name|Schema|
|---|---|
|**action**  <br>*required*|enum (read, *)|
|**object**  <br>*required*|string|


<a name="types-addpermissionforrolerequest"></a>
### types.AddPermissionForRoleRequest

|Name|Schema|
|---|---|
|**action**  <br>*required*|enum (read, *)|
|**object**  <br>*required*|string|


<a name="types-createapplicationrequest"></a>
### types.CreateApplicationRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**download_rate_limit**  <br>*optional*|integer|
|**name**  <br>*required*|string|
|**state**  <br>*optional*|enum (enable, disable)|
|**url**  <br>*optional*|string|
|**user_id**  <br>*required*|integer|


<a name="types-createconfigrequest"></a>
### types.CreateConfigRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**name**  <br>*required*|string|
|**user_id**  <br>*required*|integer|
|**value**  <br>*required*|string|


<a name="types-createjobrequest"></a>
### types.CreateJobRequest

|Name|Schema|
|---|---|
|**args**  <br>*optional*|object|
|**bio**  <br>*optional*|string|
|**result**  <br>*optional*|object|
|**scheduler_cluster_ids**  <br>*optional*|< integer > array|
|**seed_peer_cluster_ids**  <br>*optional*|< integer > array|
|**type**  <br>*required*|string|
|**user_id**  <br>*optional*|integer|


<a name="types-createoauthrequest"></a>
### types.CreateOauthRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**client_id**  <br>*required*|string|
|**client_secret**  <br>*required*|string|
|**name**  <br>*required*|enum (github, google)|
|**redirect_url**  <br>*optional*|string|


<a name="types-createrolerequest"></a>
### types.CreateRoleRequest

|Name|Schema|
|---|---|
|**permissions**  <br>*required*|< [rbac.Permission](#rbac-permission) > array|
|**role**  <br>*required*|string|


<a name="types-createschedulerclusterrequest"></a>
### types.CreateSchedulerClusterRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**client_config**  <br>*required*|[types.SchedulerClusterClientConfig](#types-schedulerclusterclientconfig)|
|**config**  <br>*required*|[types.SchedulerClusterConfig](#types-schedulerclusterconfig)|
|**is_default**  <br>*optional*|boolean|
|**name**  <br>*required*|string|
|**scopes**  <br>*optional*|[types.SchedulerClusterScopes](#types-schedulerclusterscopes)|
|**seed_peer_cluster_id**  <br>*optional*|integer|


<a name="types-createschedulerrequest"></a>
### types.CreateSchedulerRequest

|Name|Schema|
|---|---|
|**host_name**  <br>*required*|string|
|**idc**  <br>*optional*|string|
|**ip**  <br>*required*|string|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|
|**port**  <br>*required*|integer|
|**scheduler_cluster_id**  <br>*required*|integer|


<a name="types-createsecuritygrouprequest"></a>
### types.CreateSecurityGroupRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**name**  <br>*required*|string|


<a name="types-createsecurityrulerequest"></a>
### types.CreateSecurityRuleRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**domain**  <br>*required*|string|
|**name**  <br>*required*|string|
|**proxy_domain**  <br>*optional*|string|


<a name="types-createseedpeerclusterrequest"></a>
### types.CreateSeedPeerClusterRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**config**  <br>*required*|[types.SeedPeerClusterConfig](#types-seedpeerclusterconfig)|
|**is_default**  <br>*optional*|boolean|
|**name**  <br>*required*|string|
|**scopes**  <br>*optional*|[types.SeedPeerClusterScopes](#types-seedpeerclusterscopes)|


<a name="types-createseedpeerrequest"></a>
### types.CreateSeedPeerRequest

|Name|Schema|
|---|---|
|**download_port**  <br>*required*|integer|
|**host_name**  <br>*required*|string|
|**idc**  <br>*optional*|string|
|**ip**  <br>*required*|string|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|
|**port**  <br>*required*|integer|
|**seed_peer_cluster_id**  <br>*required*|integer|
|**type**  <br>*required*|enum (super, strong, weak)|


<a name="types-createv1preheatrequest"></a>
### types.CreateV1PreheatRequest

|Name|Schema|
|---|---|
|**filter**  <br>*optional*|string|
|**headers**  <br>*optional*|< string, string > map|
|**type**  <br>*required*|enum (image, file)|
|**url**  <br>*required*|string|


<a name="types-createv1preheatresponse"></a>
### types.CreateV1PreheatResponse

|Name|Schema|
|---|---|
|**id**  <br>*optional*|string|


<a name="types-deletepermissionforrolerequest"></a>
### types.DeletePermissionForRoleRequest

|Name|Schema|
|---|---|
|**action**  <br>*required*|enum (read, *)|
|**object**  <br>*required*|string|


<a name="types-getv1preheatresponse"></a>
### types.GetV1PreheatResponse

|Name|Schema|
|---|---|
|**finishTime**  <br>*optional*|string|
|**id**  <br>*optional*|string|
|**startTime**  <br>*optional*|string|
|**status**  <br>*optional*|string|


<a name="types-resetpasswordrequest"></a>
### types.ResetPasswordRequest

|Name|Description|Schema|
|---|---|---|
|**new_password**  <br>*required*|**Length** : `8 - 20`|string|
|**old_password**  <br>*required*|**Length** : `8 - 20`|string|


<a name="types-schedulerclusterclientconfig"></a>
### types.SchedulerClusterClientConfig

|Name|Description|Schema|
|---|---|---|
|**load_limit**  <br>*optional*|**Minimum value** : `1`  <br>**Maximum value** : `2000`|integer|
|**parallel_count**  <br>*optional*|**Minimum value** : `1`  <br>**Maximum value** : `50`|integer|


<a name="types-schedulerclusterconfig"></a>
### types.SchedulerClusterConfig

|Name|Description|Schema|
|---|---|---|
|**filter_parent_limit**  <br>*optional*|**Minimum value** : `1`  <br>**Maximum value** : `100`|integer|


<a name="types-schedulerclusterscopes"></a>
### types.SchedulerClusterScopes

|Name|Schema|
|---|---|
|**idc**  <br>*optional*|string|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|


<a name="types-seedpeerclusterconfig"></a>
### types.SeedPeerClusterConfig

|Name|Description|Schema|
|---|---|---|
|**load_limit**  <br>*optional*|**Minimum value** : `1`  <br>**Maximum value** : `5000`|integer|


<a name="types-seedpeerclusterscopes"></a>
### types.SeedPeerClusterScopes

|Name|Schema|
|---|---|
|**idc**  <br>*optional*|string|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|


<a name="types-signuprequest"></a>
### types.SignUpRequest

|Name|Description|Schema|
|---|---|---|
|**avatar**  <br>*optional*||string|
|**bio**  <br>*optional*||string|
|**email**  <br>*required*||string|
|**location**  <br>*optional*||string|
|**name**  <br>*required*|**Length** : `3 - 10`|string|
|**password**  <br>*required*|**Length** : `8 - 20`|string|
|**phone**  <br>*optional*||string|


<a name="types-updateapplicationrequest"></a>
### types.UpdateApplicationRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**download_rate_limit**  <br>*optional*|integer|
|**name**  <br>*optional*|string|
|**state**  <br>*optional*|enum (enable, disable)|
|**url**  <br>*optional*|string|
|**user_id**  <br>*required*|integer|


<a name="types-updateconfigrequest"></a>
### types.UpdateConfigRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**name**  <br>*optional*|string|
|**user_id**  <br>*optional*|integer|
|**value**  <br>*optional*|string|


<a name="types-updatejobrequest"></a>
### types.UpdateJobRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**user_id**  <br>*optional*|integer|


<a name="types-updateoauthrequest"></a>
### types.UpdateOauthRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**client_id**  <br>*optional*|string|
|**client_secret**  <br>*optional*|string|
|**name**  <br>*optional*|enum (github, google)|
|**redirect_url**  <br>*optional*|string|


<a name="types-updateschedulerclusterrequest"></a>
### types.UpdateSchedulerClusterRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**client_config**  <br>*optional*|[types.SchedulerClusterClientConfig](#types-schedulerclusterclientconfig)|
|**config**  <br>*optional*|[types.SchedulerClusterConfig](#types-schedulerclusterconfig)|
|**is_default**  <br>*optional*|boolean|
|**name**  <br>*optional*|string|
|**scopes**  <br>*optional*|[types.SchedulerClusterScopes](#types-schedulerclusterscopes)|
|**seed_peer_cluster_id**  <br>*optional*|integer|


<a name="types-updateschedulerrequest"></a>
### types.UpdateSchedulerRequest

|Name|Schema|
|---|---|
|**idc**  <br>*optional*|string|
|**ip**  <br>*optional*|string|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|
|**port**  <br>*optional*|integer|
|**scheduler_cluster_id**  <br>*optional*|integer|
|**scheduler_id**  <br>*optional*|integer|


<a name="types-updatesecuritygrouprequest"></a>
### types.UpdateSecurityGroupRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**name**  <br>*optional*|string|


<a name="types-updatesecurityrulerequest"></a>
### types.UpdateSecurityRuleRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**domain**  <br>*optional*|string|
|**name**  <br>*optional*|string|
|**proxy_domain**  <br>*optional*|string|


<a name="types-updateseedpeerclusterrequest"></a>
### types.UpdateSeedPeerClusterRequest

|Name|Schema|
|---|---|
|**bio**  <br>*optional*|string|
|**config**  <br>*optional*|[types.SeedPeerClusterConfig](#types-seedpeerclusterconfig)|
|**is_default**  <br>*optional*|boolean|
|**name**  <br>*optional*|string|
|**scopes**  <br>*optional*|[types.SeedPeerClusterScopes](#types-seedpeerclusterscopes)|


<a name="types-updateseedpeerrequest"></a>
### types.UpdateSeedPeerRequest

|Name|Schema|
|---|---|
|**download_port**  <br>*optional*|integer|
|**idc**  <br>*optional*|string|
|**ip**  <br>*optional*|string|
|**location**  <br>*optional*|string|
|**net_topology**  <br>*optional*|string|
|**port**  <br>*optional*|integer|
|**seed_peer_cluster_id**  <br>*optional*|integer|
|**type**  <br>*optional*|enum (super, strong, weak)|


<a name="types-updateuserrequest"></a>
### types.UpdateUserRequest

|Name|Schema|
|---|---|
|**avatar**  <br>*optional*|string|
|**bio**  <br>*optional*|string|
|**email**  <br>*optional*|string|
|**location**  <br>*optional*|string|
|**phone**  <br>*optional*|string|





