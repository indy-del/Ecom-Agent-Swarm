# 🐝 Auto-Fulfillment & Catalog Swarm (Beta)

An autonomous, multi-agent workflow designed to manage high-volume D2C e-commerce operations across decentralized storefronts (Shopify & Ecwid).

## 📌 The Problem
Managing our gourmet food brands (Indygood and Swad India) requires constant synchronization. With an active inventory of **1,700 SKUs** and an exact throughput of **1,019 monthly orders**, traditional manual management leads to API rate limits, catalog desyncs, and fulfillment delays. 

## ⚙️ Architecture & Logic Flow
We built a multi-agent system to replace manual data entry and catalog management.

1. **Ingestion & Triage Agent:** Listens to incoming webhooks from Shopify/Ecwid. It instantly parses JSON payloads to determine if the event is a catalog update or a new fulfillment request.
2. **Context & Logistics Agent:** Analyzes the fulfillment payload. It strictly filters out any anomalous COD (Cash on Delivery) flags, enforcing our rigid **prepaid-only / 0% RTO (Return to Origin)** logistics pipeline before passing data to the warehouse.
3. **Reasoning Agent (LLM Core):** For catalog updates, this agent takes raw manufacturer details and dynamically generates localized, SEO-optimized product copy for the specific SKU, standardizing tags across the 1,700-product database.
4. **Execution Agent:** Pushes the normalized payload back to the respective storefronts and triggers our automated shipping aggregator via API.

## 🚀 Why We Need High-Token Throughput
Currently, this workflow relies heavily on deterministic scripts due to token-cost limitations. Passing hundreds of JSON order payloads and full product contexts through an LLM requires massive token volume. We are actively migrating the `Reasoning Agent` to handle unstructured logistics emails and complex customer support tickets, which will consume an estimated 2M-5M tokens daily.# Ecom-Agent-Swarm
