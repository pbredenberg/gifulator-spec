# gifulator-spec

**VERSION**: 0.0.1

This project is meant to define the data specification for [Gifulator](https://github.com/pbredenberg/gifulator).

## Work In Progress

First of all, this is a work-in-progress, I've started by defining how Gifulator lists and presents gifs, later on I'll work on versioning and fleshing out this specification after studying how other web platforms and languages specify their form and function.

## 1. Purpose

In standardizing how gifs are organized and shared on the web, common clients can be created for any platform so that gifs and links to gifs can be organized however an individual likes, but still be shared and accessed easily.

## 2. Definitions

### 2.1 GIF

In the context of this specification, a GIF is a digital media file in the [Graphics Interchange Format](https://en.wikipedia.org/wiki/GIF).

## 3. URL Patterns

Gifs can be served in one of two ways:

1. In a flat directory list as served from a web server.
2. In a pageable JSON object.

### 3.1 Index

The index should start at the root directory of a server:

`https://my-gifulator.com`

### 3.2 Pages

Applications may provide a paged pattern of serving GIF indexes:

`https://my-gifulator.com/1`, `https://my-gifulator.com/2`, and so on.

An index should provide the following features:

A. Provide a way to copy the direct URL to a GIF
B. Provide a way to copy the entire GIF into the clipboard of a given device
C. Provide a hyperlink to a [GIF Presentation](#user-content-33-gif-presentation)

#### 3.2.1 Taxonomies

Applications may provide a paged taxonomy pattern of serving GIFs as secondary indexes:

`https://my-gifulator.com/my-tag-1`, `https://my-gifulator.com/my-tag-2`, and so on.

### 3.3 GIF Presentation

A single GIF's human-readable metadata and presentation should be available _directly_ from the index:

`https://my-gifulator.com/my-gif-name`

Or:

`https://my-gifulator.com/my_gif_name`

Each GIF should _not_ be available directly from a [Page](#user-content-32-pages).

**Avoid**:

`https://my-gifulator.com/1/my_gif_name`

### 3.4 Direct GIF Hyperlinks

A direct link each GIF should be available directly following GIF Presentation:

`https://my-gifulator.com/my_gif_name/my_gif_name.gif`

## 4. REST API Patterns

TODO

## 5. Clients

TODO
