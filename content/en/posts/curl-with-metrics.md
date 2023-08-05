---
title: "cURL request with metrics"
date: 2023-06-14
description: "cURL with metrics"
tags: [ "curl", "metrics", "shell" ]
category: "programming"
permalink: "curl-metrics"
published: true
---

To execute the cURL command and obtain request metrics, simply create a text file with the template below and save it
as "metrics.template.txt" (for example).

```bash
time_namelookup: %{time_namelookup}s\n
time_connect: %{time_connect}s\n
time_appconnect: %{time_appconnect}s\n
time_pretransfer: %{time_pretransfer}s\n
time_redirect: %{time_redirect}s\n
time_starttransfer: %{time_starttransfer}s\n
time_total: %{time_total}s\n
```

Then, execute the following command, replacing it with the desired URL:

```bash
curl -w "@metrics.template.txt" -o /dev/null -s "http://wordpress.com/"
```

If you prefer, you can directly execute it without the template file by adding the template's content to the `-w`
parameter, as shown in the example:

```bash
curl -w "time_namelookup: %{time_namelookup}s\n time_connect: %{time_connect}s\n time_appconnect: %{time_appconnect}s\n time_pretransfer: %{time_pretransfer}s\n time_redirect: %{time_redirect}s\n time_starttransfer: %{time_starttransfer}s\n time_total: %{time_total}s\n" -o /dev/null -s "http://wordpress.com/"
```

You can read more on [cURL docs](https://curl.se/docs/manpage.html).
