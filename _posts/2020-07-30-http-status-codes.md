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
**102** : Processing <sup>WebDAV</sup><br>
**103** : Checkpoint <sup>draft POST PUT6</sup><br>
**122** : Request-URI too long <sup>IE7</sup><br>

## 2xx: HTTP Successful Codes

**200** : OK<br>
**201** : Created<br>
**202** : Accepted<br>
**203** : Non-Authoritative Information <sup>1.1</sup><br>
**204** : No Content<br>
**205** : Reset Content<br>
**206** : Partial Content<br>
**207** : Multi Status <sup>WebDAV 4918</sup><br>
**208** : Already Reported <sup>WebDAV 5842</sup><br>
**226** : IM Used <sup>3229 GET</sup>

## 3xx: HTTP Redirection Codes

**300** : Multiple Choices<br>
**301** : Moved Permanently<br>
**302** : Found<br>
**303** : See Other <sup>1.1</sup><br>
**304** : Not Modified <br>
**305** : Use Proxy <sup>1.1</sup><br>
**306** : Switch Proxy <sup>unused</sup><br>
**307** : Temporary Redirect <sup>1.1</sup><br>
**308** : Permanent Redirect <sup>7538</sup><br>

> **307** and **308** are similiar to **302** and **301**, but the new request method after redirect must be the same, as on initial request

## 4xx: HTTP Client Error Codes

**400** : Bad Request <br>
**401** : Unauthorized <br>
**402** : Payment Required<sup>res</sup> <br>
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
**418** : I'm a teapot<sup>2324</sup> <br>
**422** : Unprocessed Entity<sup>WebDAV 4918</sup> <br>
**423** : Locked<sup>WebDAV 4918</sup> <br>
**424** : Failed Dependency<sup>WebDAV 4918</sup> <br>
**425** : Unordered Collection<sup>3648</sup> <br>
**426** : Upgrade Required<sup>2817</sup> <br>
**428** : Precondition Required<sup>draft</sup> <br>
**429** : Too Many Requests<sup>draft</sup> <br>
**431** : Request Header Fields Too Large<sup>draft</sup> <br>
**444** : No Response<sup>nginx</sup> <br>
**449** : Retry With<sup>MS</sup> <br>
**450** : Blocked By Windows Parental Control<sup>MS</sup> <br>
**451** : Unavailable For Legal Reasons<sup>MS</sup> <br>
**499** : Client Closed Request<sup>nginx</sup> <br>

# 5xx: HTTP Server Error Codes

**500** : Internal Server Error <br>
**501** : Not Implemented <br>
**502** : Bad Gateway <br>
**503** : Service Unavailable <br>
**504** : Gateway Timeout <br>
**505** : HTTP Version Not Supported<br>
**506** : Variant Also Negotiates <sup>2295</sup><br>
**507** : Insufficient Storage <sup>WebDAV 4918</sup><br>
**508** : Loop Detected<sup>WebDAV 5842ss</sup><br>
**508** : Loop Detected<sup>WebDAV 5842</sup><br>
**509** : Bandwidth Limit Exceeded<sup>nostd</sup><br>
**510** : Not Extended<sup>2774</sup><br>
**511** : Network Authentication Required<sup>draft</sup><br>
**598** : Network Read Timeout Error<sup>nostd</sup><br>
**599** : Network Connect Timeout Error<sup>nostd</sup><br>

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
