# Dragonfly Manager

<a name="overview"></a>

## 概览

Dragonfly Manager Server

### 版本信息

_版本_ : 1.0.0

### 许可信息

_许可证_ : Apache 2.0  
_服务条款_ : null

### URI scheme

_域名_ : localhost:8080  
_基础路径_ : /api/v1

<a name="paths"></a>

## 路径

<a name="api-v1-applications-post"></a>

### Create Application

```
POST /api/v1/applications
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                       | 说明        | 类型                                                                                                                      |
| -------- | -------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Body** | **Application** <br>_必填_ | Application | [d7y_io_dragonfly_v2_manager_types.CreateApplicationRequest](#d7y_io_dragonfly_v2_manager_types-createapplicationrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                            |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Application](#d7y_io_dragonfly_v2_manager_model-application) |
| **400**   | Bad Request           | 无内容                                                                                          |
| **404**   | Not Found             | 无内容                                                                                          |
| **500**   | Internal Server Error | 无内容                                                                                          |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Application

<a name="api-v1-applications-get"></a>

### Get Applications

```
GET /api/v1/applications
```

#### 说明

Get Applications

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                      |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.Application](#d7y_io_dragonfly_v2_manager_model-application) > array |
| **400**   | Bad Request           | 无内容                                                                                                    |
| **404**   | Not Found             | 无内容                                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Application

<a name="api-v1-applications-id-get"></a>

### Get Application

```
GET /api/v1/applications/{id}
```

#### 说明

Get Application by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                            |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Application](#d7y_io_dragonfly_v2_manager_model-application) |
| **400**   | Bad Request           | 无内容                                                                                          |
| **404**   | Not Found             | 无内容                                                                                          |
| **500**   | Internal Server Error | 无内容                                                                                          |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Application

<a name="api-v1-applications-id-delete"></a>

### Destroy Application

```
DELETE /api/v1/applications/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Application

<a name="api-v1-applications-id-patch"></a>

### Update Application

```
PATCH /api/v1/applications/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                       | 说明        | 类型                                                                                                                      |
| -------- | -------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_          | id          | string                                                                                                                    |
| **Body** | **Application** <br>_必填_ | Application | [d7y_io_dragonfly_v2_manager_types.UpdateApplicationRequest](#d7y_io_dragonfly_v2_manager_types-updateapplicationrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                            |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Application](#d7y_io_dragonfly_v2_manager_model-application) |
| **400**   | Bad Request           | 无内容                                                                                          |
| **404**   | Not Found             | 无内容                                                                                          |
| **500**   | Internal Server Error | 无内容                                                                                          |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Application

<a name="api-v1-buckets-post"></a>

### Create Bucket

```
POST /api/v1/buckets
```

#### 说明

Create by json bucket

#### 参数

| 类型     | 名称                  | 说明   | 类型                                                                                                            |
| -------- | --------------------- | ------ | --------------------------------------------------------------------------------------------------------------- |
| **Body** | **Bucket** <br>_必填_ | Bucket | [d7y_io_dragonfly_v2_manager_types.CreateBucketRequest](#d7y_io_dragonfly_v2_manager_types-createbucketrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Bucket

<a name="api-v1-buckets-get"></a>

### Get Buckets

```
GET /api/v1/buckets
```

#### 说明

Get Buckets

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                                    |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_pkg_objectstorage.BucketMetadata](#d7y_io_dragonfly_v2_pkg_objectstorage-bucketmetadata) > array |
| **400**   | Bad Request           | 无内容                                                                                                                  |
| **404**   | Not Found             | 无内容                                                                                                                  |
| **500**   | Internal Server Error | 无内容                                                                                                                  |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Bucket

<a name="api-v1-buckets-id-get"></a>

### Get Bucket

```
GET /api/v1/buckets/{id}
```

#### 说明

Get Bucket by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                          |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_pkg_objectstorage.BucketMetadata](#d7y_io_dragonfly_v2_pkg_objectstorage-bucketmetadata) |
| **400**   | Bad Request           | 无内容                                                                                                        |
| **404**   | Not Found             | 无内容                                                                                                        |
| **500**   | Internal Server Error | 无内容                                                                                                        |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Bucket

<a name="api-v1-buckets-id-delete"></a>

### Destroy Bucket

```
DELETE /api/v1/buckets/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Bucket

<a name="api-v1-configs-post"></a>

### Create Config

```
POST /api/v1/configs
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                  | 说明   | 类型                                                                                                            |
| -------- | --------------------- | ------ | --------------------------------------------------------------------------------------------------------------- |
| **Body** | **Config** <br>_必填_ | Config | [d7y_io_dragonfly_v2_manager_types.CreateConfigRequest](#d7y_io_dragonfly_v2_manager_types-createconfigrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                  |
| --------- | --------------------- | ------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Config](#d7y_io_dragonfly_v2_manager_model-config) |
| **400**   | Bad Request           | 无内容                                                                                |
| **404**   | Not Found             | 无内容                                                                                |
| **500**   | Internal Server Error | 无内容                                                                                |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Config

<a name="api-v1-configs-get"></a>

### Get Configs

```
GET /api/v1/configs
```

#### 说明

Get Configs

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                            |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.Config](#d7y_io_dragonfly_v2_manager_model-config) > array |
| **400**   | Bad Request           | 无内容                                                                                          |
| **404**   | Not Found             | 无内容                                                                                          |
| **500**   | Internal Server Error | 无内容                                                                                          |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Config

<a name="api-v1-configs-id-get"></a>

### Get Config

```
GET /api/v1/configs/{id}
```

#### 说明

Get Config by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                  |
| --------- | --------------------- | ------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Config](#d7y_io_dragonfly_v2_manager_model-config) |
| **400**   | Bad Request           | 无内容                                                                                |
| **404**   | Not Found             | 无内容                                                                                |
| **500**   | Internal Server Error | 无内容                                                                                |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Config

<a name="api-v1-configs-id-delete"></a>

### Destroy Config

```
DELETE /api/v1/configs/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Config

<a name="api-v1-configs-id-patch"></a>

### Update Config

```
PATCH /api/v1/configs/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                  | 说明   | 类型                                                                                                            |
| -------- | --------------------- | ------ | --------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_     | id     | string                                                                                                          |
| **Body** | **Config** <br>_必填_ | Config | [d7y_io_dragonfly_v2_manager_types.UpdateConfigRequest](#d7y_io_dragonfly_v2_manager_types-updateconfigrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                  |
| --------- | --------------------- | ------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Config](#d7y_io_dragonfly_v2_manager_model-config) |
| **400**   | Bad Request           | 无内容                                                                                |
| **404**   | Not Found             | 无内容                                                                                |
| **500**   | Internal Server Error | 无内容                                                                                |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Config

<a name="api-v1-healthy-get"></a>

### Get Health

```
GET /api/v1/healthy
```

#### 说明

Get app health

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Health

<a name="api-v1-jobs-post"></a>

### Create Job

```
POST /api/v1/jobs
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称               | 说明 | 类型                                                                                                      |
| -------- | ------------------ | ---- | --------------------------------------------------------------------------------------------------------- |
| **Body** | **Job** <br>_必填_ | Job  | [d7y_io_dragonfly_v2_manager_types.CreateJobRequest](#d7y_io_dragonfly_v2_manager_types-createjobrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                            |
| --------- | --------------------- | ------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Job](#d7y_io_dragonfly_v2_manager_model-job) |
| **400**   | Bad Request           | 无内容                                                                          |
| **404**   | Not Found             | 无内容                                                                          |
| **500**   | Internal Server Error | 无内容                                                                          |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Job

<a name="api-v1-jobs-get"></a>

### Get Jobs

```
GET /api/v1/jobs
```

#### 说明

Get Jobs

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                      |
| --------- | --------------------- | ----------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.Job](#d7y_io_dragonfly_v2_manager_model-job) > array |
| **400**   | Bad Request           | 无内容                                                                                    |
| **404**   | Not Found             | 无内容                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Job

<a name="api-v1-jobs-id-get"></a>

### Get Job

```
GET /api/v1/jobs/{id}
```

#### 说明

Get Job by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                            |
| --------- | --------------------- | ------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Job](#d7y_io_dragonfly_v2_manager_model-job) |
| **400**   | Bad Request           | 无内容                                                                          |
| **404**   | Not Found             | 无内容                                                                          |
| **500**   | Internal Server Error | 无内容                                                                          |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Job

<a name="api-v1-jobs-id-delete"></a>

### Destroy Job

```
DELETE /api/v1/jobs/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Job

<a name="api-v1-jobs-id-patch"></a>

### Update Job

```
PATCH /api/v1/jobs/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称               | 说明 | 类型                                                                                                      |
| -------- | ------------------ | ---- | --------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_  | id   | string                                                                                                    |
| **Body** | **Job** <br>_必填_ | Job  | [d7y_io_dragonfly_v2_manager_types.UpdateJobRequest](#d7y_io_dragonfly_v2_manager_types-updatejobrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                            |
| --------- | --------------------- | ------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Job](#d7y_io_dragonfly_v2_manager_model-job) |
| **400**   | Bad Request           | 无内容                                                                          |
| **404**   | Not Found             | 无内容                                                                          |
| **500**   | Internal Server Error | 无内容                                                                          |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Job

<a name="api-v1-oauth-post"></a>

### Create Oauth

```
POST /api/v1/oauth
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                 | 说明  | 类型                                                                                                          |
| -------- | -------------------- | ----- | ------------------------------------------------------------------------------------------------------------- |
| **Body** | **Oauth** <br>_必填_ | Oauth | [d7y_io_dragonfly_v2_manager_types.CreateOauthRequest](#d7y_io_dragonfly_v2_manager_types-createoauthrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                |
| --------- | --------------------- | ----------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Oauth](#d7y_io_dragonfly_v2_manager_model-oauth) |
| **400**   | Bad Request           | 无内容                                                                              |
| **404**   | Not Found             | 无内容                                                                              |
| **500**   | Internal Server Error | 无内容                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Oauth

<a name="api-v1-oauth-get"></a>

### Get Oauths

```
GET /api/v1/oauth
```

#### 说明

Get Oauths

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                          |
| --------- | --------------------- | --------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.Oauth](#d7y_io_dragonfly_v2_manager_model-oauth) > array |
| **400**   | Bad Request           | 无内容                                                                                        |
| **404**   | Not Found             | 无内容                                                                                        |
| **500**   | Internal Server Error | 无内容                                                                                        |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Oauth

<a name="api-v1-oauth-id-get"></a>

### Get Oauth

```
GET /api/v1/oauth/{id}
```

#### 说明

Get Oauth by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                |
| --------- | --------------------- | ----------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Oauth](#d7y_io_dragonfly_v2_manager_model-oauth) |
| **400**   | Bad Request           | 无内容                                                                              |
| **404**   | Not Found             | 无内容                                                                              |
| **500**   | Internal Server Error | 无内容                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Oauth

<a name="api-v1-oauth-id-delete"></a>

### Destroy Oauth

```
DELETE /api/v1/oauth/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Oauth

<a name="api-v1-oauth-id-patch"></a>

### Update Oauth

```
PATCH /api/v1/oauth/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                 | 说明  | 类型                                                                                                          |
| -------- | -------------------- | ----- | ------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_    | id    | string                                                                                                        |
| **Body** | **Oauth** <br>_必填_ | Oauth | [d7y_io_dragonfly_v2_manager_types.UpdateOauthRequest](#d7y_io_dragonfly_v2_manager_types-updateoauthrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                |
| --------- | --------------------- | ----------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Oauth](#d7y_io_dragonfly_v2_manager_model-oauth) |
| **400**   | Bad Request           | 无内容                                                                              |
| **404**   | Not Found             | 无内容                                                                              |
| **500**   | Internal Server Error | 无内容                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Oauth

<a name="api-v1-peers-get"></a>

### Get Peers

```
GET /api/v1/peers
```

#### 说明

Get Peers

#### 响应

| HTTP 代码 | 说明                  | 类型             |
| --------- | --------------------- | ---------------- |
| **200**   | OK                    | < string > array |
| **400**   | Bad Request           | 无内容           |
| **404**   | Not Found             | 无内容           |
| **500**   | Internal Server Error | 无内容           |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Peer

<a name="api-v1-permissions-get"></a>

### Get Permissions

```
GET /api/v1/permissions
```

#### 说明

Get Permissions

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                                        |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_permission_rbac.Permission](#d7y_io_dragonfly_v2_manager_permission_rbac-permission) > array |
| **400**   | Bad Request           | 无内容                                                                                                                      |
| **500**   | Internal Server Error | 无内容                                                                                                                      |

#### 生成

- `application/json`

#### 标签

- Permission

<a name="api-v1-preheats-post"></a>

### Create V1 Preheat

```
POST /api/v1/preheats
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                   | 说明    | 类型                                                                                                                  |
| -------- | ---------------------- | ------- | --------------------------------------------------------------------------------------------------------------------- |
| **Body** | **Preheat** <br>_必填_ | Preheat | [d7y_io_dragonfly_v2_manager_types.CreateV1PreheatRequest](#d7y_io_dragonfly_v2_manager_types-createv1preheatrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                                    |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.CreateV1PreheatResponse](#d7y_io_dragonfly_v2_manager_types-createv1preheatresponse) |
| **400**   | Bad Request           | 无内容                                                                                                                  |
| **404**   | Not Found             | 无内容                                                                                                                  |
| **500**   | Internal Server Error | 无内容                                                                                                                  |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Preheat

<a name="api-v1-preheats-id-get"></a>

### Get V1 Preheat

```
GET /api/v1/preheats/{id}
```

#### 说明

Get Preheat by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                              |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.GetV1PreheatResponse](#d7y_io_dragonfly_v2_manager_types-getv1preheatresponse) |
| **400**   | Bad Request           | 无内容                                                                                                            |
| **404**   | Not Found             | 无内容                                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Preheat

<a name="api-v1-roles-post"></a>

### Create Role

```
POST /api/v1/roles
```

#### 说明

Create Role by json config

#### 参数

| 类型     | 名称                | 说明 | 类型                                                                                                        |
| -------- | ------------------- | ---- | ----------------------------------------------------------------------------------------------------------- |
| **Body** | **Role** <br>_必填_ | Role | [d7y_io_dragonfly_v2_manager_types.CreateRoleRequest](#d7y_io_dragonfly_v2_manager_types-createrolerequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Role

<a name="api-v1-roles-get"></a>

### Get Roles

```
GET /api/v1/roles
```

#### 说明

Get roles

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Role

<a name="api-v1-roles-role-get"></a>

### Get Role

```
GET /api/v1/roles/{role}
```

#### 说明

Get Role

#### 参数

| 类型     | 名称                | 说明 | 类型   |
| -------- | ------------------- | ---- | ------ |
| **Path** | **role** <br>_必填_ | role | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Role

<a name="api-v1-roles-role-delete"></a>

### Destroy Role

```
DELETE /api/v1/roles/{role}
```

#### 说明

Destroy role by json config

#### 参数

| 类型     | 名称                | 说明 | 类型   |
| -------- | ------------------- | ---- | ------ |
| **Path** | **role** <br>_必填_ | role | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Role

<a name="api-v1-roles-role-permissions-post"></a>

### Add Permission For Role

```
POST /api/v1/roles/{role}/permissions
```

#### 说明

Add Permission by json config

#### 参数

| 类型     | 名称                      | 说明       | 类型                                                                                                                            |
| -------- | ------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **role** <br>_必填_       | role       | string                                                                                                                          |
| **Body** | **Permission** <br>_必填_ | Permission | [d7y_io_dragonfly_v2_manager_types.AddPermissionForRoleRequest](#d7y_io_dragonfly_v2_manager_types-addpermissionforrolerequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Role

<a name="api-v1-roles-role-permissions-delete"></a>

### Update Role

```
DELETE /api/v1/roles/{role}/permissions
```

#### 说明

Remove Role Permission by json config

#### 参数

| 类型     | 名称                      | 说明       | 类型                                                                                                                                  |
| -------- | ------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **role** <br>_必填_       | role       | string                                                                                                                                |
| **Body** | **Permission** <br>_必填_ | Permission | [d7y_io_dragonfly_v2_manager_types.DeletePermissionForRoleRequest](#d7y_io_dragonfly_v2_manager_types-deletepermissionforrolerequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Role

<a name="api-v1-scheduler-clusters-post"></a>

### Create SchedulerCluster

```
POST /api/v1/scheduler-clusters
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                            | 说明             | 类型                                                                                                                                |
| -------- | ------------------------------- | ---------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Body** | **SchedulerCluster** <br>_必填_ | SchedulerCluster | [d7y_io_dragonfly_v2_manager_types.CreateSchedulerClusterRequest](#d7y_io_dragonfly_v2_manager_types-createschedulerclusterrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                      |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SchedulerCluster](#d7y_io_dragonfly_v2_manager_model-schedulercluster) |
| **400**   | Bad Request           | 无内容                                                                                                    |
| **404**   | Not Found             | 无内容                                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SchedulerCluster

<a name="api-v1-scheduler-clusters-get"></a>

### Get SchedulerClusters

```
GET /api/v1/scheduler-clusters
```

#### 说明

Get SchedulerClusters

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                                |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.SchedulerCluster](#d7y_io_dragonfly_v2_manager_model-schedulercluster) > array |
| **400**   | Bad Request           | 无内容                                                                                                              |
| **404**   | Not Found             | 无内容                                                                                                              |
| **500**   | Internal Server Error | 无内容                                                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SchedulerCluster

<a name="api-v1-scheduler-clusters-id-get"></a>

### Get SchedulerCluster

```
GET /api/v1/scheduler-clusters/{id}
```

#### 说明

Get SchedulerCluster by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                      |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SchedulerCluster](#d7y_io_dragonfly_v2_manager_model-schedulercluster) |
| **400**   | Bad Request           | 无内容                                                                                                    |
| **404**   | Not Found             | 无内容                                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SchedulerCluster

<a name="api-v1-scheduler-clusters-id-delete"></a>

### Destroy SchedulerCluster

```
DELETE /api/v1/scheduler-clusters/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SchedulerCluster

<a name="api-v1-scheduler-clusters-id-patch"></a>

### Update SchedulerCluster

```
PATCH /api/v1/scheduler-clusters/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                            | 说明             | 类型                                                                                                                                |
| -------- | ------------------------------- | ---------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_               | id               | string                                                                                                                              |
| **Body** | **SchedulerCluster** <br>_必填_ | SchedulerCluster | [d7y_io_dragonfly_v2_manager_types.UpdateSchedulerClusterRequest](#d7y_io_dragonfly_v2_manager_types-updateschedulerclusterrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                      |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SchedulerCluster](#d7y_io_dragonfly_v2_manager_model-schedulercluster) |
| **400**   | Bad Request           | 无内容                                                                                                    |
| **404**   | Not Found             | 无内容                                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SchedulerCluster

<a name="api-v1-scheduler-clusters-id-schedulers-scheduler_id-put"></a>

### Add Scheduler to schedulerCluster

```
PUT /api/v1/scheduler-clusters/{id}/schedulers/{scheduler_id}
```

#### 说明

Add Scheduler to schedulerCluster

#### 参数

| 类型     | 名称                        | 说明         | 类型   |
| -------- | --------------------------- | ------------ | ------ |
| **Path** | **id** <br>_必填_           | id           | string |
| **Path** | **scheduler_id** <br>_必填_ | scheduler id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SchedulerCluster

<a name="api-v1-schedulers-post"></a>

### Create Scheduler

```
POST /api/v1/schedulers
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                     | 说明      | 类型                                                                                                                  |
| -------- | ------------------------ | --------- | --------------------------------------------------------------------------------------------------------------------- |
| **Body** | **Scheduler** <br>_必填_ | Scheduler | [d7y_io_dragonfly_v2_manager_types.CreateSchedulerRequest](#d7y_io_dragonfly_v2_manager_types-createschedulerrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                        |
| --------- | --------------------- | ------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Scheduler](#d7y_io_dragonfly_v2_manager_model-scheduler) |
| **400**   | Bad Request           | 无内容                                                                                      |
| **404**   | Not Found             | 无内容                                                                                      |
| **500**   | Internal Server Error | 无内容                                                                                      |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Scheduler

<a name="api-v1-schedulers-get"></a>

### Get Schedulers

```
GET /api/v1/schedulers
```

#### 说明

Get Schedulers

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                  |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.Scheduler](#d7y_io_dragonfly_v2_manager_model-scheduler) > array |
| **400**   | Bad Request           | 无内容                                                                                                |
| **404**   | Not Found             | 无内容                                                                                                |
| **500**   | Internal Server Error | 无内容                                                                                                |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Scheduler

<a name="api-v1-schedulers-id-get"></a>

### Get Scheduler

```
GET /api/v1/schedulers/{id}
```

#### 说明

Get Scheduler by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                        |
| --------- | --------------------- | ------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Scheduler](#d7y_io_dragonfly_v2_manager_model-scheduler) |
| **400**   | Bad Request           | 无内容                                                                                      |
| **404**   | Not Found             | 无内容                                                                                      |
| **500**   | Internal Server Error | 无内容                                                                                      |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Scheduler

<a name="api-v1-schedulers-id-delete"></a>

### Destroy Scheduler

```
DELETE /api/v1/schedulers/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Scheduler

<a name="api-v1-schedulers-id-patch"></a>

### Update Scheduler

```
PATCH /api/v1/schedulers/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                     | 说明      | 类型                                                                                                                  |
| -------- | ------------------------ | --------- | --------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_        | id        | string                                                                                                                |
| **Body** | **Scheduler** <br>_必填_ | Scheduler | [d7y_io_dragonfly_v2_manager_types.UpdateSchedulerRequest](#d7y_io_dragonfly_v2_manager_types-updateschedulerrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                        |
| --------- | --------------------- | ------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.Scheduler](#d7y_io_dragonfly_v2_manager_model-scheduler) |
| **400**   | Bad Request           | 无内容                                                                                      |
| **404**   | Not Found             | 无内容                                                                                      |
| **500**   | Internal Server Error | 无内容                                                                                      |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Scheduler

<a name="api-v1-schedulers-id-models-post"></a>

### Create Model

```
POST /api/v1/schedulers/{id}/models
```

#### 说明

Create by id

#### 参数

| 类型     | 名称                 | 说明  | 类型                                                                                                          |
| -------- | -------------------- | ----- | ------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_    | id    | string                                                                                                        |
| **Body** | **Model** <br>_必填_ | Model | [d7y_io_dragonfly_v2_manager_types.CreateModelRequest](#d7y_io_dragonfly_v2_manager_types-createmodelrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                |
| --------- | --------------------- | ----------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.Model](#d7y_io_dragonfly_v2_manager_types-model) |
| **400**   | Bad Request           | 无内容                                                                              |
| **404**   | Not Found             | 无内容                                                                              |
| **500**   | Internal Server Error | 无内容                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-get"></a>

### Get Models

```
GET /api/v1/schedulers/{id}/models
```

#### 说明

Get Models

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                          |
| --------- | --------------------- | --------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_types.Model](#d7y_io_dragonfly_v2_manager_types-model) > array |
| **400**   | Bad Request           | 无内容                                                                                        |
| **404**   | Not Found             | 无内容                                                                                        |
| **500**   | Internal Server Error | 无内容                                                                                        |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-get"></a>

### Get Model

```
GET /api/v1/schedulers/{id}/models/{model_id}
```

#### 说明

Get Model by id

#### 参数

| 类型     | 名称                    | 说明     | 类型   |
| -------- | ----------------------- | -------- | ------ |
| **Path** | **id** <br>_必填_       | id       | string |
| **Path** | **model_id** <br>_必填_ | model_id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                |
| --------- | --------------------- | ----------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.Model](#d7y_io_dragonfly_v2_manager_types-model) |
| **400**   | Bad Request           | 无内容                                                                              |
| **404**   | Not Found             | 无内容                                                                              |
| **500**   | Internal Server Error | 无内容                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-delete"></a>

### Destroy Model

```
DELETE /api/v1/schedulers/{id}/models/{model_id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称                    | 说明     | 类型   |
| -------- | ----------------------- | -------- | ------ |
| **Path** | **id** <br>_必填_       | id       | string |
| **Path** | **model_id** <br>_必填_ | model_id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-patch"></a>

### Update Model

```
PATCH /api/v1/schedulers/{id}/models/{model_id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                    | 说明     | 类型                                                                                                          |
| -------- | ----------------------- | -------- | ------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_       | id       | string                                                                                                        |
| **Path** | **model_id** <br>_必填_ | model_id | string                                                                                                        |
| **Body** | **Model** <br>_必填_    | Model    | [d7y_io_dragonfly_v2_manager_types.UpdateModelRequest](#d7y_io_dragonfly_v2_manager_types-updatemodelrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                |
| --------- | --------------------- | ----------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.Model](#d7y_io_dragonfly_v2_manager_types-model) |
| **400**   | Bad Request           | 无内容                                                                              |
| **404**   | Not Found             | 无内容                                                                              |
| **500**   | Internal Server Error | 无内容                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-versions-post"></a>

### Create Model Version

```
POST /api/v1/schedulers/{id}/models/{model_id}/versions
```

#### 说明

Create by id

#### 参数

| 类型     | 名称                        | 说明         | 类型                                                                                                                        |
| -------- | --------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_           | id           | string                                                                                                                      |
| **Path** | **model_id** <br>_必填_     | model_id     | string                                                                                                                      |
| **Body** | **ModelVersion** <br>_必填_ | ModelVersion | [d7y_io_dragonfly_v2_manager_types.CreateModelVersionRequest](#d7y_io_dragonfly_v2_manager_types-createmodelversionrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                              |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.ModelVersion](#d7y_io_dragonfly_v2_manager_types-modelversion) |
| **400**   | Bad Request           | 无内容                                                                                            |
| **404**   | Not Found             | 无内容                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-versions-get"></a>

### Get Model Versions

```
GET /api/v1/schedulers/{id}/models/{model_id}/versions
```

#### 说明

Get Model Versions by id

#### 参数

| 类型     | 名称                    | 说明     | 类型   |
| -------- | ----------------------- | -------- | ------ |
| **Path** | **id** <br>_必填_       | id       | string |
| **Path** | **model_id** <br>_必填_ | model_id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                        |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_types.ModelVersion](#d7y_io_dragonfly_v2_manager_types-modelversion) > array |
| **400**   | Bad Request           | 无内容                                                                                                      |
| **404**   | Not Found             | 无内容                                                                                                      |
| **500**   | Internal Server Error | 无内容                                                                                                      |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-versions-version_id-get"></a>

### Get Model Version

```
GET /api/v1/schedulers/{id}/models/{model_id}/versions/{version_id}
```

#### 说明

Get Model Version by id

#### 参数

| 类型     | 名称                      | 说明       | 类型   |
| -------- | ------------------------- | ---------- | ------ |
| **Path** | **id** <br>_必填_         | id         | string |
| **Path** | **model_id** <br>_必填_   | model_id   | string |
| **Path** | **version_id** <br>_必填_ | version_id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                              |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.ModelVersion](#d7y_io_dragonfly_v2_manager_types-modelversion) |
| **400**   | Bad Request           | 无内容                                                                                            |
| **404**   | Not Found             | 无内容                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-versions-version_id-delete"></a>

### Destroy Model Version

```
DELETE /api/v1/schedulers/{id}/models/{model_id}/versions/{version_id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称                      | 说明       | 类型   |
| -------- | ------------------------- | ---------- | ------ |
| **Path** | **id** <br>_必填_         | id         | string |
| **Path** | **model_id** <br>_必填_   | model_id   | string |
| **Path** | **version_id** <br>_必填_ | version_id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-schedulers-id-models-model_id-versions-version_id-patch"></a>

### Update Model Version

```
PATCH /api/v1/schedulers/{id}/models/{model_id}/versions/{version_id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                        | 说明         | 类型                                                                                                                        |
| -------- | --------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_           | id           | string                                                                                                                      |
| **Path** | **model_id** <br>_必填_     | model_id     | string                                                                                                                      |
| **Path** | **version_id** <br>_必填_   | version_id   | string                                                                                                                      |
| **Body** | **ModelVersion** <br>_必填_ | ModelVersion | [d7y_io_dragonfly_v2_manager_types.UpdateModelVersionRequest](#d7y_io_dragonfly_v2_manager_types-updatemodelversionrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                              |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_types.ModelVersion](#d7y_io_dragonfly_v2_manager_types-modelversion) |
| **400**   | Bad Request           | 无内容                                                                                            |
| **404**   | Not Found             | 无内容                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Model

<a name="api-v1-security-groups-post"></a>

### Create SecurityGroup

```
POST /api/v1/security-groups
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                         | 说明          | 类型                                                                                                                          |
| -------- | ---------------------------- | ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Body** | **SecurityGroup** <br>_必填_ | SecurityGroup | [d7y_io_dragonfly_v2_manager_types.CreateSecurityGroupRequest](#d7y_io_dragonfly_v2_manager_types-createsecuritygrouprequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SecurityGroup](#d7y_io_dragonfly_v2_manager_model-securitygroup) |
| **400**   | Bad Request           | 无内容                                                                                              |
| **404**   | Not Found             | 无内容                                                                                              |
| **500**   | Internal Server Error | 无内容                                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-groups-get"></a>

### Get SecurityGroups

```
GET /api/v1/security-groups
```

#### 说明

Get SecurityGroups

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                          |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.SecurityGroup](#d7y_io_dragonfly_v2_manager_model-securitygroup) > array |
| **400**   | Bad Request           | 无内容                                                                                                        |
| **404**   | Not Found             | 无内容                                                                                                        |
| **500**   | Internal Server Error | 无内容                                                                                                        |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-groups-id-get"></a>

### Get SecurityGroup

```
GET /api/v1/security-groups/{id}
```

#### 说明

Get SecurityGroup by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SecurityGroup](#d7y_io_dragonfly_v2_manager_model-securitygroup) |
| **400**   | Bad Request           | 无内容                                                                                              |
| **404**   | Not Found             | 无内容                                                                                              |
| **500**   | Internal Server Error | 无内容                                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-groups-id-patch"></a>

### Update SecurityGroup

```
PATCH /api/v1/security-groups/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                         | 说明          | 类型                                                                                                                          |
| -------- | ---------------------------- | ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_            | id            | string                                                                                                                        |
| **Body** | **SecurityGroup** <br>_必填_ | SecurityGroup | [d7y_io_dragonfly_v2_manager_types.UpdateSecurityGroupRequest](#d7y_io_dragonfly_v2_manager_types-updatesecuritygrouprequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SecurityGroup](#d7y_io_dragonfly_v2_manager_model-securitygroup) |
| **400**   | Bad Request           | 无内容                                                                                              |
| **404**   | Not Found             | 无内容                                                                                              |
| **500**   | Internal Server Error | 无内容                                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-groups-id-scheduler-clusters-scheduler_cluster_id-put"></a>

### Add Scheduler to SecurityGroup

```
PUT /api/v1/security-groups/{id}/scheduler-clusters/{scheduler_cluster_id}
```

#### 说明

Add Scheduler to SecurityGroup

#### 参数

| 类型     | 名称                                | 说明                 | 类型   |
| -------- | ----------------------------------- | -------------------- | ------ |
| **Path** | **id** <br>_必填_                   | id                   | string |
| **Path** | **scheduler_cluster_id** <br>_必填_ | scheduler cluster id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-groups-id-security-rules-security_rule_id-put"></a>

### Add SecurityRule to SecurityGroup

```
PUT /api/v1/security-groups/{id}/security-rules/{security_rule_id}
```

#### 说明

Add SecurityRule to SecurityGroup

#### 参数

| 类型     | 名称                            | 说明             | 类型   |
| -------- | ------------------------------- | ---------------- | ------ |
| **Path** | **id** <br>_必填_               | id               | string |
| **Path** | **security_rule_id** <br>_必填_ | security rule id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-groups-id-security-rules-security_rule_id-delete"></a>

### Destroy SecurityRule to SecurityGroup

```
DELETE /api/v1/security-groups/{id}/security-rules/{security_rule_id}
```

#### 说明

Destroy SecurityRule to SecurityGroup

#### 参数

| 类型     | 名称                            | 说明             | 类型   |
| -------- | ------------------------------- | ---------------- | ------ |
| **Path** | **id** <br>_必填_               | id               | string |
| **Path** | **security_rule_id** <br>_必填_ | security rule id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-groups-id-seed-peer-clusters-seed_peer_cluster_id-put"></a>

### Add SeedPeer to SecurityGroup

```
PUT /api/v1/security-groups/{id}/seed-peer-clusters/{seed_peer_cluster_id}
```

#### 说明

Add SeedPeer to SecurityGroup

#### 参数

| 类型     | 名称                                | 说明                 | 类型   |
| -------- | ----------------------------------- | -------------------- | ------ |
| **Path** | **id** <br>_必填_                   | id                   | string |
| **Path** | **seed_peer_cluster_id** <br>_必填_ | seed peer cluster id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-security-rules-post"></a>

### Create SecurityRule

```
POST /api/v1/security-rules
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                        | 说明         | 类型                                                                                                                        |
| -------- | --------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------- |
| **Body** | **SecurityRule** <br>_必填_ | SecurityRule | [d7y_io_dragonfly_v2_manager_types.CreateSecurityRuleRequest](#d7y_io_dragonfly_v2_manager_types-createsecurityrulerequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                              |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SecurityRule](#d7y_io_dragonfly_v2_manager_model-securityrule) |
| **400**   | Bad Request           | 无内容                                                                                            |
| **404**   | Not Found             | 无内容                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityRule

<a name="api-v1-security-rules-get"></a>

### Get SecurityRules

```
GET /api/v1/security-rules
```

#### 说明

Get SecurityRules

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                        |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.SecurityRule](#d7y_io_dragonfly_v2_manager_model-securityrule) > array |
| **400**   | Bad Request           | 无内容                                                                                                      |
| **404**   | Not Found             | 无内容                                                                                                      |
| **500**   | Internal Server Error | 无内容                                                                                                      |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityRule

<a name="api-v1-security-rules-id-get"></a>

### Get SecurityRule

```
GET /api/v1/security-rules/{id}
```

#### 说明

Get SecurityRule by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                              |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SecurityRule](#d7y_io_dragonfly_v2_manager_model-securityrule) |
| **400**   | Bad Request           | 无内容                                                                                            |
| **404**   | Not Found             | 无内容                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityRule

<a name="api-v1-security-rules-id-patch"></a>

### Update SecurityRule

```
PATCH /api/v1/security-rules/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                        | 说明         | 类型                                                                                                                        |
| -------- | --------------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_           | id           | string                                                                                                                      |
| **Body** | **SecurityRule** <br>_必填_ | SecurityRule | [d7y_io_dragonfly_v2_manager_types.UpdateSecurityRuleRequest](#d7y_io_dragonfly_v2_manager_types-updatesecurityrulerequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                              |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SecurityRule](#d7y_io_dragonfly_v2_manager_model-securityrule) |
| **400**   | Bad Request           | 无内容                                                                                            |
| **404**   | Not Found             | 无内容                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityRule

<a name="api-v1-securitygroups-id-delete"></a>

### Destroy SecurityGroup

```
DELETE /api/v1/securityGroups/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityGroup

<a name="api-v1-securityrules-id-delete"></a>

### Destroy SecurityRule

```
DELETE /api/v1/securityRules/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SecurityRule

<a name="api-v1-seed-peer-clusters-post"></a>

### Create SeedPeerCluster

```
POST /api/v1/seed-peer-clusters
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                           | 说明      | 类型                                                                                                                              |
| -------- | ------------------------------ | --------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Body** | **SeedPeerCluster** <br>_必填_ | DNCluster | [d7y_io_dragonfly_v2_manager_types.CreateSeedPeerClusterRequest](#d7y_io_dragonfly_v2_manager_types-createseedpeerclusterrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                    |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SeedPeerCluster](#d7y_io_dragonfly_v2_manager_model-seedpeercluster) |
| **400**   | Bad Request           | 无内容                                                                                                  |
| **404**   | Not Found             | 无内容                                                                                                  |
| **500**   | Internal Server Error | 无内容                                                                                                  |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeerCluster

<a name="api-v1-seed-peer-clusters-get"></a>

### Get SeedPeerClusters

```
GET /api/v1/seed-peer-clusters
```

#### 说明

Get SeedPeerClusters

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                              |
| --------- | --------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.SeedPeerCluster](#d7y_io_dragonfly_v2_manager_model-seedpeercluster) > array |
| **400**   | Bad Request           | 无内容                                                                                                            |
| **404**   | Not Found             | 无内容                                                                                                            |
| **500**   | Internal Server Error | 无内容                                                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeerCluster

<a name="api-v1-seed-peer-clusters-id-get"></a>

### Get SeedPeerCluster

```
GET /api/v1/seed-peer-clusters/{id}
```

#### 说明

Get SeedPeerCluster by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                    |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SeedPeerCluster](#d7y_io_dragonfly_v2_manager_model-seedpeercluster) |
| **400**   | Bad Request           | 无内容                                                                                                  |
| **404**   | Not Found             | 无内容                                                                                                  |
| **500**   | Internal Server Error | 无内容                                                                                                  |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeerCluster

<a name="api-v1-seed-peer-clusters-id-delete"></a>

### Destroy SeedPeerCluster

```
DELETE /api/v1/seed-peer-clusters/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeerCluster

<a name="api-v1-seed-peer-clusters-id-patch"></a>

### Update SeedPeerCluster

```
PATCH /api/v1/seed-peer-clusters/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                           | 说明            | 类型                                                                                                                              |
| -------- | ------------------------------ | --------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_              | id              | string                                                                                                                            |
| **Body** | **SeedPeerCluster** <br>_必填_ | SeedPeerCluster | [d7y_io_dragonfly_v2_manager_types.UpdateSeedPeerClusterRequest](#d7y_io_dragonfly_v2_manager_types-updateseedpeerclusterrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                    |
| --------- | --------------------- | ------------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SeedPeerCluster](#d7y_io_dragonfly_v2_manager_model-seedpeercluster) |
| **400**   | Bad Request           | 无内容                                                                                                  |
| **404**   | Not Found             | 无内容                                                                                                  |
| **500**   | Internal Server Error | 无内容                                                                                                  |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeerCluster

<a name="api-v1-seed-peer-clusters-id-scheduler-clusters-scheduler_cluster_id-put"></a>

### Add SchedulerCluster to SeedPeerCluster

```
PUT /api/v1/seed-peer-clusters/{id}/scheduler-clusters/{scheduler_cluster_id}
```

#### 说明

Add SchedulerCluster to SeedPeerCluster

#### 参数

| 类型     | 名称                                | 说明                 | 类型   |
| -------- | ----------------------------------- | -------------------- | ------ |
| **Path** | **id** <br>_必填_                   | id                   | string |
| **Path** | **scheduler_cluster_id** <br>_必填_ | scheduler cluster id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeerCluster

<a name="api-v1-seed-peer-clusters-id-seed-peers-seed_peer_id-put"></a>

### Add Instance to SeedPeerCluster

```
PUT /api/v1/seed-peer-clusters/{id}/seed-peers/{seed_peer_id}
```

#### 说明

Add SeedPeer to SeedPeerCluster

#### 参数

| 类型     | 名称                        | 说明         | 类型   |
| -------- | --------------------------- | ------------ | ------ |
| **Path** | **id** <br>_必填_           | id           | string |
| **Path** | **seed_peer_id** <br>_必填_ | seed peer id | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeerCluster

<a name="api-v1-seed-peers-post"></a>

### Create SeedPeer

```
POST /api/v1/seed-peers
```

#### 说明

Create by json config

#### 参数

| 类型     | 名称                    | 说明     | 类型                                                                                                                |
| -------- | ----------------------- | -------- | ------------------------------------------------------------------------------------------------------------------- |
| **Body** | **SeedPeer** <br>_必填_ | SeedPeer | [d7y_io_dragonfly_v2_manager_types.CreateSeedPeerRequest](#d7y_io_dragonfly_v2_manager_types-createseedpeerrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                      |
| --------- | --------------------- | ----------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SeedPeer](#d7y_io_dragonfly_v2_manager_model-seedpeer) |
| **400**   | Bad Request           | 无内容                                                                                    |
| **404**   | Not Found             | 无内容                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeer

<a name="api-v1-seed-peers-get"></a>

### Get SeedPeers

```
GET /api/v1/seed-peers
```

#### 说明

Get SeedPeers

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                                |
| --------- | --------------------- | --------------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.SeedPeer](#d7y_io_dragonfly_v2_manager_model-seedpeer) > array |
| **400**   | Bad Request           | 无内容                                                                                              |
| **404**   | Not Found             | 无内容                                                                                              |
| **500**   | Internal Server Error | 无内容                                                                                              |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeer

<a name="api-v1-seed-peers-id-get"></a>

### Get SeedPeer

```
GET /api/v1/seed-peers/{id}
```

#### 说明

Get SeedPeer by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                      |
| --------- | --------------------- | ----------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SeedPeer](#d7y_io_dragonfly_v2_manager_model-seedpeer) |
| **400**   | Bad Request           | 无内容                                                                                    |
| **404**   | Not Found             | 无内容                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeer

<a name="api-v1-seed-peers-id-delete"></a>

### Destroy SeedPeer

```
DELETE /api/v1/seed-peers/{id}
```

#### 说明

Destroy by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeer

<a name="api-v1-seed-peers-id-patch"></a>

### Update SeedPeer

```
PATCH /api/v1/seed-peers/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                    | 说明     | 类型                                                                                                                |
| -------- | ----------------------- | -------- | ------------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_       | id       | string                                                                                                              |
| **Body** | **SeedPeer** <br>_必填_ | SeedPeer | [d7y_io_dragonfly_v2_manager_types.UpdateSeedPeerRequest](#d7y_io_dragonfly_v2_manager_types-updateseedpeerrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                      |
| --------- | --------------------- | ----------------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.SeedPeer](#d7y_io_dragonfly_v2_manager_model-seedpeer) |
| **400**   | Bad Request           | 无内容                                                                                    |
| **404**   | Not Found             | 无内容                                                                                    |
| **500**   | Internal Server Error | 无内容                                                                                    |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- SeedPeer

<a name="api-v1-user-signin-name-get"></a>

### Oauth Signin

```
GET /api/v1/user/signin/{name}
```

#### 说明

oauth signin by json config

#### 参数

| 类型     | 名称                | 说明 | 类型   |
| -------- | ------------------- | ---- | ------ |
| **Path** | **name** <br>_必填_ | name | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- User

<a name="api-v1-user-signin-name-callback-get"></a>

### Oauth Signin Callback

```
GET /api/v1/user/signin/{name}/callback
```

#### 说明

oauth signin callback by json config

#### 参数

| 类型      | 名称                | 说明 | 类型   |
| --------- | ------------------- | ---- | ------ |
| **Path**  | **name** <br>_必填_ | name | string |
| **Query** | **code** <br>_必填_ | code | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **404**   | Not Found             | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 标签

- Oauth

<a name="api-v1-user-signup-post"></a>

### SignUp user

```
POST /api/v1/user/signup
```

#### 说明

signup by json config

#### 参数

| 类型     | 名称                | 说明 | 类型                                                                                                |
| -------- | ------------------- | ---- | --------------------------------------------------------------------------------------------------- |
| **Body** | **User** <br>_必填_ | User | [d7y_io_dragonfly_v2_manager_types.SignUpRequest](#d7y_io_dragonfly_v2_manager_types-signuprequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                              |
| --------- | --------------------- | --------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.User](#d7y_io_dragonfly_v2_manager_model-user) |
| **400**   | Bad Request           | 无内容                                                                            |
| **500**   | Internal Server Error | 无内容                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- User

<a name="api-v1-users-get"></a>

### Get Users

```
GET /api/v1/users
```

#### 说明

Get Users

#### 参数

| 类型      | 名称                    | 说明                                      | 类型    | 默认值 |
| --------- | ----------------------- | ----------------------------------------- | ------- | ------ |
| **Query** | **page** <br>_必填_     | current page                              | integer | `0`    |
| **Query** | **per_page** <br>_必填_ | return max item count, default 10, max 50 | integer | `10`   |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                                        |
| --------- | --------------------- | ------------------------------------------------------------------------------------------- |
| **200**   | OK                    | < [d7y_io_dragonfly_v2_manager_model.User](#d7y_io_dragonfly_v2_manager_model-user) > array |
| **400**   | Bad Request           | 无内容                                                                                      |
| **404**   | Not Found             | 无内容                                                                                      |
| **500**   | Internal Server Error | 无内容                                                                                      |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- User

<a name="api-v1-users-id-get"></a>

### Get User

```
GET /api/v1/users/{id}
```

#### 说明

Get User by id

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                              |
| --------- | --------------------- | --------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.User](#d7y_io_dragonfly_v2_manager_model-user) |
| **400**   | Bad Request           | 无内容                                                                            |
| **404**   | Not Found             | 无内容                                                                            |
| **500**   | Internal Server Error | 无内容                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- User

<a name="api-v1-users-id-patch"></a>

### Update User

```
PATCH /api/v1/users/{id}
```

#### 说明

Update by json config

#### 参数

| 类型     | 名称                | 说明 | 类型                                                                                                        |
| -------- | ------------------- | ---- | ----------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_   | id   | string                                                                                                      |
| **Body** | **User** <br>_必填_ | User | [d7y_io_dragonfly_v2_manager_types.UpdateUserRequest](#d7y_io_dragonfly_v2_manager_types-updateuserrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型                                                                              |
| --------- | --------------------- | --------------------------------------------------------------------------------- |
| **200**   | OK                    | [d7y_io_dragonfly_v2_manager_model.User](#d7y_io_dragonfly_v2_manager_model-user) |
| **400**   | Bad Request           | 无内容                                                                            |
| **404**   | Not Found             | 无内容                                                                            |
| **500**   | Internal Server Error | 无内容                                                                            |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- User

<a name="api-v1-users-id-reset_password-post"></a>

### Reset Password For User

```
POST /api/v1/users/{id}/reset_password
```

#### 说明

reset password by json config

#### 参数

| 类型     | 名称                | 说明 | 类型                                                                                                              |
| -------- | ------------------- | ---- | ----------------------------------------------------------------------------------------------------------------- |
| **Path** | **id** <br>_必填_   | id   | integer                                                                                                           |
| **Body** | **User** <br>_必填_ | User | [d7y_io_dragonfly_v2_manager_types.ResetPasswordRequest](#d7y_io_dragonfly_v2_manager_types-resetpasswordrequest) |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- User

<a name="api-v1-users-id-roles-get"></a>

### Get User Roles

```
GET /api/v1/users/{id}/roles
```

#### 说明

get roles by json config

#### 参数

| 类型     | 名称              | 说明 | 类型   |
| -------- | ----------------- | ---- | ------ |
| **Path** | **id** <br>_必填_ | id   | string |

#### 响应

| HTTP 代码 | 说明                  | 类型             |
| --------- | --------------------- | ---------------- |
| **200**   | OK                    | < string > array |
| **400**   | Bad Request           | 无内容           |
| **500**   | Internal Server Error | 无内容           |

#### 生成

- `application/json`

#### 标签

- User

<a name="api-v1-users-id-roles-role-put"></a>

### Add Role For User

```
PUT /api/v1/users/{id}/roles/{role}
```

#### 说明

add role to user by uri config

#### 参数

| 类型     | 名称                | 说明 | 类型   |
| -------- | ------------------- | ---- | ------ |
| **Path** | **id** <br>_必填_   | id   | string |
| **Path** | **role** <br>_必填_ | role | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Users

<a name="api-v1-users-id-roles-role-delete"></a>

### Delete Role For User

```
DELETE /api/v1/users/{id}/roles/{role}
```

#### 说明

delete role by uri config

#### 参数

| 类型     | 名称                | 说明 | 类型   |
| -------- | ------------------- | ---- | ------ |
| **Path** | **id** <br>_必填_   | id   | string |
| **Path** | **role** <br>_必填_ | role | string |

#### 响应

| HTTP 代码 | 说明                  | 类型   |
| --------- | --------------------- | ------ |
| **200**   | OK                    | 无内容 |
| **400**   | Bad Request           | 无内容 |
| **500**   | Internal Server Error | 无内容 |

#### 消耗

- `application/json`

#### 生成

- `application/json`

#### 标签

- Users
