---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "mimir_alertmanager_config Data Source - terraform-provider-mimir"
subcategory: ""
description: |-
  
---

# mimir_alertmanager_config (Data Source)

## Basic Example

```hcl
data "mimir_alertmanager_config" "mytenant" {}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Read-Only

- `global` (List of Object) (see [below for nested schema](#nestedatt--global))
- `id` (String) The ID of this resource.
- `inhibit_rule` (List of Object) Mutes an alert (target) matching a set of matchers when an alert (source) exists that matches another set of matchers. (see [below for nested schema](#nestedatt--inhibit_rule))
- `receiver` (List of Object) A list of notification receivers. (see [below for nested schema](#nestedatt--receiver))
- `route` (List of Object) The root node of the routing tree. (see [below for nested schema](#nestedatt--route))
- `templates` (List of String) A list of template names to use.
- `templates_files` (Map of String) A map of key values string, where the key is the template name and the value the content of the template.
- `time_interval` (List of Object) A list of time intervals for muting/activating routes. (see [below for nested schema](#nestedatt--time_interval))

<a id="nestedatt--global"></a>
### Nested Schema for `global`

Read-Only:

- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--global--http_config))
- `opsgenie_api_key` (String)
- `opsgenie_api_url` (String)
- `pagerduty_url` (String)
- `resolve_timeout` (String)
- `slack_api_url` (String)
- `smtp_auth_identity` (String)
- `smtp_auth_password` (String)
- `smtp_auth_secret` (String)
- `smtp_auth_username` (String)
- `smtp_from` (String)
- `smtp_hello` (String)
- `smtp_require_tls` (Boolean)
- `smtp_smarthost` (String)
- `telegram_api_url` (String)
- `victorops_api_key` (String)
- `victorops_api_url` (String)
- `wechat_api_corp_id` (String)
- `wechat_api_secret` (String)
- `wechat_api_url` (String)

<a id="nestedobjatt--global--http_config"></a>
### Nested Schema for `global.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--global--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--global--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--global--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--global--http_config--tls_config))

<a id="nestedobjatt--global--http_config--authorization"></a>
### Nested Schema for `global.http_config.authorization`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--global--http_config--basic_auth"></a>
### Nested Schema for `global.http_config.basic_auth`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--global--http_config--oauth2"></a>
### Nested Schema for `global.http_config.oauth2`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--global--http_config--oauth2--tls_config))
- `token_url` (String)

<a id="nestedobjatt--global--http_config--oauth2--tls_config"></a>
### Nested Schema for `global.http_config.oauth2.token_url`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--global--http_config--tls_config"></a>
### Nested Schema for `global.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)




<a id="nestedatt--inhibit_rule"></a>
### Nested Schema for `inhibit_rule`

Read-Only:

- `equal` (List of String)
- `source_matchers` (List of String)
- `target_matchers` (List of String)


<a id="nestedatt--receiver"></a>
### Nested Schema for `receiver`

Read-Only:

- `email_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--email_configs))
- `name` (String)
- `opsgenie_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs))
- `pagerduty_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs))
- `pushover_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pushover_configs))
- `slack_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs))
- `sns_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs))
- `telegram_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--telegram_configs))
- `victorops_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--victorops_configs))
- `webhook_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--webhook_configs))
- `wechat_configs` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--wechat_configs))

<a id="nestedobjatt--receiver--email_configs"></a>
### Nested Schema for `receiver.email_configs`

Read-Only:

- `auth_identity` (String)
- `auth_password` (String)
- `auth_secret` (String)
- `auth_username` (String)
- `from` (String)
- `headers` (Map of String)
- `hello` (String)
- `html` (String)
- `require_tls` (Boolean)
- `send_resolved` (Boolean)
- `smarthost` (String)
- `text` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--email_configs--tls_config))
- `to` (String)

<a id="nestedobjatt--receiver--email_configs--tls_config"></a>
### Nested Schema for `receiver.email_configs.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--opsgenie_configs"></a>
### Nested Schema for `receiver.opsgenie_configs`

Read-Only:

- `actions` (String)
- `api_key` (String)
- `api_url` (String)
- `description` (String)
- `details` (Map of String)
- `entity` (String)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs--http_config))
- `message` (String)
- `note` (String)
- `priority` (String)
- `responders` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs--responders))
- `send_resolved` (Boolean)
- `source` (String)
- `tags` (String)
- `update_alerts` (String)

<a id="nestedobjatt--receiver--opsgenie_configs--http_config"></a>
### Nested Schema for `receiver.opsgenie_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--opsgenie_configs--http_config--authorization"></a>
### Nested Schema for `receiver.opsgenie_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--opsgenie_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.opsgenie_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--opsgenie_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.opsgenie_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--opsgenie_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--opsgenie_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.opsgenie_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--opsgenie_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.opsgenie_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--opsgenie_configs--responders"></a>
### Nested Schema for `receiver.opsgenie_configs.responders`

Read-Only:

- `id` (String)
- `name` (String)
- `type` (String)
- `username` (String)



<a id="nestedobjatt--receiver--pagerduty_configs"></a>
### Nested Schema for `receiver.pagerduty_configs`

Read-Only:

- `class` (String)
- `client` (String)
- `client_url` (String)
- `component` (String)
- `description` (String)
- `details` (Map of String)
- `group` (String)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--http_config))
- `images` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--images))
- `links` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--links))
- `routing_key` (String)
- `send_resolved` (Boolean)
- `service_key` (String)
- `severity` (String)
- `url` (String)

<a id="nestedobjatt--receiver--pagerduty_configs--http_config"></a>
### Nested Schema for `receiver.pagerduty_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--pagerduty_configs--http_config--authorization"></a>
### Nested Schema for `receiver.pagerduty_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--pagerduty_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.pagerduty_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--pagerduty_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.pagerduty_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pagerduty_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--pagerduty_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.pagerduty_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--pagerduty_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.pagerduty_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--pagerduty_configs--images"></a>
### Nested Schema for `receiver.pagerduty_configs.images`

Read-Only:

- `alt` (String)
- `href` (String)
- `src` (String)


<a id="nestedobjatt--receiver--pagerduty_configs--links"></a>
### Nested Schema for `receiver.pagerduty_configs.links`

Read-Only:

- `href` (String)
- `text` (String)



<a id="nestedobjatt--receiver--pushover_configs"></a>
### Nested Schema for `receiver.pushover_configs`

Read-Only:

- `expire` (String)
- `html` (Boolean)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pushover_configs--http_config))
- `message` (String)
- `priority` (String)
- `retry` (String)
- `send_resolved` (Boolean)
- `sound` (String)
- `title` (String)
- `token` (String)
- `url` (String)
- `url_title` (String)
- `user_key` (String)

<a id="nestedobjatt--receiver--pushover_configs--http_config"></a>
### Nested Schema for `receiver.pushover_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pushover_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pushover_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pushover_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pushover_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--pushover_configs--http_config--authorization"></a>
### Nested Schema for `receiver.pushover_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--pushover_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.pushover_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--pushover_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.pushover_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--pushover_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--pushover_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.pushover_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--pushover_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.pushover_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)




<a id="nestedobjatt--receiver--slack_configs"></a>
### Nested Schema for `receiver.slack_configs`

Read-Only:

- `actions` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--actions))
- `api_url` (String)
- `callback_id` (String)
- `channel` (String)
- `color` (String)
- `fallback` (String)
- `fields` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--fields))
- `footer` (String)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--http_config))
- `icon_emoji` (String)
- `icon_url` (String)
- `image_url` (String)
- `link_names` (Boolean)
- `mrkdwn_in` (List of String)
- `pretext` (String)
- `send_resolved` (Boolean)
- `short_fields` (Boolean)
- `text` (String)
- `thumb_url` (String)
- `title` (String)
- `title_link` (String)
- `username` (String)

<a id="nestedobjatt--receiver--slack_configs--actions"></a>
### Nested Schema for `receiver.slack_configs.actions`

Read-Only:

- `confirm` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--actions--confirm))
- `name` (String)
- `style` (String)
- `text` (String)
- `type` (String)
- `url` (String)
- `value` (String)

<a id="nestedobjatt--receiver--slack_configs--actions--confirm"></a>
### Nested Schema for `receiver.slack_configs.actions.value`

Read-Only:

- `dismiss_text` (String)
- `ok_text` (String)
- `text` (String)
- `title` (String)



<a id="nestedobjatt--receiver--slack_configs--fields"></a>
### Nested Schema for `receiver.slack_configs.fields`

Read-Only:

- `short` (Boolean)
- `title` (String)
- `value` (String)


<a id="nestedobjatt--receiver--slack_configs--http_config"></a>
### Nested Schema for `receiver.slack_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--slack_configs--http_config--authorization"></a>
### Nested Schema for `receiver.slack_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--slack_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.slack_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--slack_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.slack_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--slack_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--slack_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.slack_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--slack_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.slack_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)




<a id="nestedobjatt--receiver--sns_configs"></a>
### Nested Schema for `receiver.sns_configs`

Read-Only:

- `api_url` (String)
- `attributes` (Map of String)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs--http_config))
- `message` (String)
- `phone_number` (String)
- `send_resolved` (Boolean)
- `sigv4` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs--sigv4))
- `subject` (String)
- `target_arn` (String)
- `topic_arn` (String)

<a id="nestedobjatt--receiver--sns_configs--http_config"></a>
### Nested Schema for `receiver.sns_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--sns_configs--http_config--authorization"></a>
### Nested Schema for `receiver.sns_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--sns_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.sns_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--sns_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.sns_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--sns_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--sns_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.sns_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--sns_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.sns_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--sns_configs--sigv4"></a>
### Nested Schema for `receiver.sns_configs.sigv4`

Read-Only:

- `access_key` (String)
- `profile` (String)
- `region` (String)
- `role_arn` (String)
- `secret_key` (String)



<a id="nestedobjatt--receiver--telegram_configs"></a>
### Nested Schema for `receiver.telegram_configs`

Read-Only:

- `api_url` (String)
- `bot_token` (String)
- `chat_id` (String)
- `disable_notifications` (Boolean)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--telegram_configs--http_config))
- `message` (String)
- `parse_mode` (String)
- `send_resolved` (Boolean)

<a id="nestedobjatt--receiver--telegram_configs--http_config"></a>
### Nested Schema for `receiver.telegram_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--telegram_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--telegram_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--telegram_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--telegram_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--telegram_configs--http_config--authorization"></a>
### Nested Schema for `receiver.telegram_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--telegram_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.telegram_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--telegram_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.telegram_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--telegram_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--telegram_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.telegram_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--telegram_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.telegram_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)




<a id="nestedobjatt--receiver--victorops_configs"></a>
### Nested Schema for `receiver.victorops_configs`

Read-Only:

- `api_key` (String)
- `api_url` (String)
- `custom_fields` (Map of String)
- `entity_display_name` (String)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--victorops_configs--http_config))
- `message_type` (String)
- `monitoring_tool` (String)
- `routing_key` (String)
- `send_resolved` (Boolean)
- `state_message` (String)

<a id="nestedobjatt--receiver--victorops_configs--http_config"></a>
### Nested Schema for `receiver.victorops_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--victorops_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--victorops_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--victorops_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--victorops_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--victorops_configs--http_config--authorization"></a>
### Nested Schema for `receiver.victorops_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--victorops_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.victorops_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--victorops_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.victorops_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--victorops_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--victorops_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.victorops_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--victorops_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.victorops_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)




<a id="nestedobjatt--receiver--webhook_configs"></a>
### Nested Schema for `receiver.webhook_configs`

Read-Only:

- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--webhook_configs--http_config))
- `max_alerts` (Number)
- `send_resolved` (Boolean)
- `url` (String)

<a id="nestedobjatt--receiver--webhook_configs--http_config"></a>
### Nested Schema for `receiver.webhook_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--webhook_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--webhook_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--webhook_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--webhook_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--webhook_configs--http_config--authorization"></a>
### Nested Schema for `receiver.webhook_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--webhook_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.webhook_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--webhook_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.webhook_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--webhook_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--webhook_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.webhook_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--webhook_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.webhook_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)




<a id="nestedobjatt--receiver--wechat_configs"></a>
### Nested Schema for `receiver.wechat_configs`

Read-Only:

- `agent_id` (String)
- `api_secret` (String)
- `api_url` (String)
- `corp_id` (String)
- `http_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--wechat_configs--http_config))
- `message` (String)
- `message_type` (String)
- `send_resolved` (Boolean)
- `to_party` (String)
- `to_tag` (String)
- `to_user` (String)

<a id="nestedobjatt--receiver--wechat_configs--http_config"></a>
### Nested Schema for `receiver.wechat_configs.http_config`

Read-Only:

- `authorization` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--wechat_configs--http_config--authorization))
- `basic_auth` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--wechat_configs--http_config--basic_auth))
- `bearer_token` (String)
- `follow_redirects` (Boolean)
- `oauth2` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--wechat_configs--http_config--oauth2))
- `proxy_url` (String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--wechat_configs--http_config--tls_config))

<a id="nestedobjatt--receiver--wechat_configs--http_config--authorization"></a>
### Nested Schema for `receiver.wechat_configs.http_config.tls_config`

Read-Only:

- `credentials` (String)
- `type` (String)


<a id="nestedobjatt--receiver--wechat_configs--http_config--basic_auth"></a>
### Nested Schema for `receiver.wechat_configs.http_config.tls_config`

Read-Only:

- `password` (String)
- `username` (String)


<a id="nestedobjatt--receiver--wechat_configs--http_config--oauth2"></a>
### Nested Schema for `receiver.wechat_configs.http_config.tls_config`

Read-Only:

- `client_id` (String)
- `client_secret` (String)
- `endpoint_params` (Map of String)
- `scopes` (List of String)
- `tls_config` (List of Object) (see [below for nested schema](#nestedobjatt--receiver--wechat_configs--http_config--tls_config--tls_config))
- `token_url` (String)

<a id="nestedobjatt--receiver--wechat_configs--http_config--tls_config--tls_config"></a>
### Nested Schema for `receiver.wechat_configs.http_config.tls_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)



<a id="nestedobjatt--receiver--wechat_configs--http_config--tls_config"></a>
### Nested Schema for `receiver.wechat_configs.http_config.tls_config`

Read-Only:

- `insecure_skip_verify` (Boolean)
- `server_name` (String)





<a id="nestedatt--route"></a>
### Nested Schema for `route`

Read-Only:

- `child_route` (List of Object) (see [below for nested schema](#nestedobjatt--route--child_route))
- `continue` (Boolean)
- `group_by` (List of String)
- `group_interval` (String)
- `group_wait` (String)
- `receiver` (String)
- `repeat_interval` (String)

<a id="nestedobjatt--route--child_route"></a>
### Nested Schema for `route.child_route`

Read-Only:

- `active_time_intervals` (List of String)
- `continue` (Boolean)
- `group_by` (List of String)
- `group_interval` (String)
- `group_wait` (String)
- `matchers` (List of String)
- `mute_time_intervals` (List of String)
- `receiver` (String)
- `repeat_interval` (String)



<a id="nestedatt--time_interval"></a>
### Nested Schema for `time_interval`

Read-Only:

- `name` (String)
- `time_intervals` (List of Object) (see [below for nested schema](#nestedobjatt--time_interval--time_intervals))

<a id="nestedobjatt--time_interval--time_intervals"></a>
### Nested Schema for `time_interval.time_intervals`

Read-Only:

- `days_of_month` (List of Object) (see [below for nested schema](#nestedobjatt--time_interval--time_intervals--days_of_month))
- `months` (List of Object) (see [below for nested schema](#nestedobjatt--time_interval--time_intervals--months))
- `times` (List of Object) (see [below for nested schema](#nestedobjatt--time_interval--time_intervals--times))
- `weekdays` (List of Object) (see [below for nested schema](#nestedobjatt--time_interval--time_intervals--weekdays))
- `years` (List of Object) (see [below for nested schema](#nestedobjatt--time_interval--time_intervals--years))

<a id="nestedobjatt--time_interval--time_intervals--days_of_month"></a>
### Nested Schema for `time_interval.time_intervals.days_of_month`

Read-Only:

- `begin` (Number)
- `end` (Number)


<a id="nestedobjatt--time_interval--time_intervals--months"></a>
### Nested Schema for `time_interval.time_intervals.months`

Read-Only:

- `begin` (Number)
- `end` (Number)


<a id="nestedobjatt--time_interval--time_intervals--times"></a>
### Nested Schema for `time_interval.time_intervals.times`

Read-Only:

- `end_minute` (Number)
- `start_minute` (Number)


<a id="nestedobjatt--time_interval--time_intervals--weekdays"></a>
### Nested Schema for `time_interval.time_intervals.weekdays`

Read-Only:

- `begin` (Number)
- `end` (Number)


<a id="nestedobjatt--time_interval--time_intervals--years"></a>
### Nested Schema for `time_interval.time_intervals.years`

Read-Only:

- `begin` (Number)
- `end` (Number)

