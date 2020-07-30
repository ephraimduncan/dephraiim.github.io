---
layout: post
title: HTTPS Status Codes
subtitle: 404 Not Found
tags: [HTTPS, API, REST]
author: Ephraim Atta-Duncan
comments: True
---

# HTTPS / REST Status Codes

## 1xx: HTTP Informational Codes

**100** : Continue<br>
**101** : Switching Protocols<br>
**102** : Processing `WebDAV`<br>
**103** : Checkpoint `draft POST PUT6`<br>
**122** : Request-URI too long `IE7`<br>

## 2xx: HTTP Successful Codes

**200** : OK<br>
**201** : Created<br>
**202** : Accepted<br>
**203** : Non-Authoritative Information `1.1`<br>
**204** : No Content<br>
**205** : Reset Content<br>
**206** : Partial Content<br>
**207** : Multi Status `WebDAV 4918`<br>
**208** : Already Reported `WebDAV 5842`<br>
**226** : IM Used `3229 GET`

## 3xx: HTTP Redirection Codes

**300** : Multiple Choices<br>
**301** : Moved Permanently<br>
**302** : Found<br>
**303** : See Other `1.1`<br>
**304** : Not Modified <br>
**305** : Use Proxy `1.1`<br>
**306** : Switch Proxy `unused`<br>
**307** : Temporary Redirect `1.1`<br>
**308** : Permanent Redirect `7538`<br>

> **307** and **308** are similiar to **302** and **301**, but the new request method after redirect must be the same, as on initial request

## 4xx: HTTP Client Error Codes

**400** : Bad Request <br>
**401** : Unauthorized <br>
**402** : Payment Required `res` <br>
**403** : Forbidden <br>
**404** : Not Found <br>
**405** : Method Not Allowed <br>
**406** : Not Acceptable <br>
**407** : Proxy Authentication Required <br>
**408** : Request Timeout <br>
**409** : Conflict <br>
**410** : Gone <br>
**411** : Length Required <br>
**412** : Precondition Failed <br>
**413** : Request Entity Too Large <br>
**414** : Request-URI Too Long <br>
**415** : Unsupported Media Type <br>
**416** : Request Range Not Satisfiable <br>
**417** : Exception Failed <br>
**418** : I'm a teapot `2324` <br>
**422** : Unprocessed Entity `WebDAV 4918` <br>
**423** : Locked `WebDAV 4918` <br>
**424** : Failed Dependency `WebDAV 4918` <br>
**425** : Unordered Collection `3648` <br>
**426** : Upgrade Required `2817` <br>
**428** : Precondition Required `draft` <br>
**429** : Too Many Requests `draft` <br>
**431** : Request Header Fields Too Large `draft` <br>
**444** : No Response `nginx` <br>
**449** : Retry With `MS` <br>
**450** : Blocked By Windows Parental Control `MS` <br>
**451** : Unavailable For Legal Reasons `MS` <br>
**499** : Client Closed Request `nginx` <br>

# 5xx: HTTP Server Error Codes

**500** : Internal Server Error <br>
**501** : Not Implemented <br>
**502** : Bad Gateway <br>
**503** : Service Unavailable <br>
**504** : Gateway Timeout <br>
**505** : HTTP Version Not Supported<br>
**506** : Variant Also Negotiates `2295`<br>
**507** : Insufficient Storage `WebDAV 4918`<br>
**508** : Loop Detected `WebDAV 5842ss`<br>
**508** : Loop Detected `WebDAV 5842`<br>
**509** : Bandwidth Limit Exceeded `nostd`<br>
**510** : Not Extended `2774`<br>
**511** : Network Authentication Required `draft`<br>
**598** : Network Read Timeout Error `nostd`<br>
**599** : Network Connect Timeout Error `nostd`<br>

## HTTP Code Comments

**WebDAV** : WebDAV Extension <br>
**1.1** : HTTP/1.1 <br>
**IE** : IE Extension <br>
**MS** : MS Extension <br>
**nginx** : nginx Extension <br>
**2518, 2817, 2995, 2774, 3229, 4918, 5842** : RFC Number <br>
**draft** : Proposed Draft <br>
**nostd** : Non Standard Extension <br>
**res** : Reserved for future use <br>
**unused** : No more in use [deprecated]<br>
