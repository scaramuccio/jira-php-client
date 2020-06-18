# jira-php-client
PHP client for Jira

## Usage
```php
<?php

use Scaramuccio\Jira\JiraClientFactory;

$client = JiraClientFactory::create([
    'authentication_credentials' => 'Bearer',
    'authentication_scheme' => 'abc',
    'base_uri' => 'https://mycompany.atlassian.net'
]);

$client->createIssue(...);
```

## Configuration

The following configuration options are available for instantiating `JiraClient`:

| Option | Type | Description |
|---|---|---|
| `authentication_credentials` | string | `Basic`, `Bearer`, ... |
| `authentication_scheme`      | string | Bearer token, base64-encoded username and password, ... |
| `base_uri`                   | string | Base URI of the Jira instance. E.g. `https://mycompany.atlassian.net` |
| `connection_timeout`         | int    | The number of seconds until the connection times out. Defaults to 5. |
| `http_proxy`                 | string | HTTP proxy to be used. E.g. `user:pass@192.168.0.1` |
| `https_proxy`                | string | HTTPS proxy to be used. E.g. `user:pass@192.168.0.1` |
| `no_proxy`                   | string | Addresses where no proxy is to be used, in an array. E.g. `["192.168.0.2", "192.168.0.3"]` |