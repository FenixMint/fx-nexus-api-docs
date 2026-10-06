# FX NEXUS — Allegro REST API integration

## Purpose

FX NEXUS is an internal application used for the owner's own Allegro account.

The current Allegro integration is used to read Allegro product catalogue data, identify products and enrich product information used while preparing Allegro offers locally in FX NEXUS.

At the current stage, the integration does **not** create, edit, activate or publish Allegro offers through the REST API.

## Current scope

The current integration uses Allegro REST API for read-only technical operations related to product data, including:

- searching the Allegro product catalogue,
- reading product details,
- identifying products by catalogue identifiers,
- comparing and enriching product data,
- validating product information before an Allegro offer is prepared,
- supporting local preparation and development of Allegro offer content.

Offer titles, descriptions, technical parameters, product identity data and other offer content may be prepared locally in FX NEXUS before any publication step.

The current API connection is not used for seller-side offer writes.

## Authentication

The application uses OAuth 2.0 Device Authorization Grant (Device Flow).

Credentials and access tokens are stored locally in the application environment and are not published in source code or documentation.

## Intended use

The integration is used only for the owner's own business operations and own Allegro account. It is not offered as a service for third-party sellers.

The current Allegro API connection is read-only and supports product-data access and local offer preparation.

Direct seller-side publication through the Allegro REST API is not enabled in the current version.

## Offer preparation

FX NEXUS prepares Allegro offer data locally before publication.

This may include:

- product identification,
- catalogue matching,
- product-data verification,
- technical parameter preparation,
- offer title preparation,
- offer description preparation,
- validation of product and offer data,
- preparation of a complete offer draft for later use on Allegro.

Local preparation does not itself create or activate an offer on Allegro.

## Security and access control

FX NEXUS applies the following principles:

- minimum required API permissions,
- read-only access for the current Allegro technical integration,
- no storage of API secrets in public documentation or source code,
- verification of product identity before offer preparation,
- local validation of offer data before any future external write capability is used.

## Application

**Name:** FX NEXUS  
**Type:** internal/local application  
**Use:** own Allegro account  
**Current Allegro API mode:** read-only product catalogue and product-data operations  
**Current use of offer data:** local preparation and validation  
**Offer publication through the current Allegro API connection:** no

## Contact

Project owner / repository owner: **FenixMint**

This document describes the current intended use of the Allegro REST API integration and may be updated when the integration scope changes.
