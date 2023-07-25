---
template: overrides/main.html
title: Ledgers
---

# Ledgers

Ledgers in Cellmobs function as a comprehensive financial log that captures all the monetary transactions within an application. This includes capturing [payment transactions](/app-console/manage-orders/#payment-transactions) related to [product](/app-console/manage-products) orders from certain vendors, an attribute associated with Organizations that participate in a Cellmobs [Marketplace](/guide/marketplaces) or [E-Commerce](/guide/e-commerce) application.

Ledgers can also document the revenue and cost elements related to order servicing and collaborations with business partners. While the use of Ledgers is optional, having an [Organization](/app-console/manage-organizations) entity configured with a primary Ledger simplifies financial tracking. Once this configuration is set, all the monetary data tied to that Organization will automatically flow into the designated Ledger.

This ability to track financial flows effectively becomes particularly significant for financial analyses and reports. By having a complete record of revenues, costs in the Ledger, it becomes easier to generate meaningful financial insights and reports. For example the sytem can generate profit sharing reports between provided that the terms of any agreements between the involved Organizations (such as Vendors, Customers, Suppliers) have been properly logged as [Deals](/app-console/manage-ledgers#Deals).

Ledgers in Cellmobs offer a high degree of flexibility, allowing users to not only track internal financial transactions but also to import entries from external sources. Users can add data to ledgers through CSV imports, making it easier to centralize financial information from various sources in a single location. This can be particularly useful when dealing with multiple channels or platforms where financial transactions occur. Or with revenue statements received by business partners. 

Additionally, ledgers can be updated with financial data received via [API integrations](/app-console/manage-integrations) from other applications and integrations. This seamless connection between systems ensures that your financial records around cost and revenues related to Products are centralized and always up-to-date, minimizing the potential for discrepancies or missing data.

Moreover, the information captured in these ledgers can also be synchronized with popular accounting software like Intuit's Quicken and QuickBooks (Coming soon). This will enable a streamlined workflow, allowing businesses to seamlessly move financial data between their operational platform and their accounting system.

## Reports

Cellmobs allows for extensive reporting from transaction Ledgers. This includes not only standard financial reports like product and customer revenue summaries, but also complex revenue sharing reports based on the terms of agreements between multiple stakeholders such as suppliers, vendors, distributors, agents, and sellers.

A key component of the financial system is its concept of "Deals". Deals in Cellmobs serve as comprehensive documentation of the terms of an agreement between multiple organizations. For instance, a Deal might outline the revenue sharing agreement between a supplier and a distributor, or between an agent and a seller. 

To generate financial reports, Cellmobs automatically collects and organizes all financial data related to these Deals into Ledgers. This includes everything from payment transactions associated with product orders, to the costs and revenues associated with servicing orders or dealing with business partners. Once an Organization is configured with a primary Ledger, all this data flows automatically into it, providing a complete financial overview.

From these detailed Ledgers, Cellmobs is then able to generate a variety of financial reports. 

- **Product and Customer Revenue Summaries:** Cellmobs can quickly pull data from the Ledgers to produce summaries of revenues from different products or customers, giving businesses key insights into their most profitable areas.

- **Revenue Sharing Reports:** Perhaps most powerful is Cellmobs' ability to produce revenue sharing reports. These reports detail how revenues are divided between different parties based on the terms outlined in their Deals. For instance, if a supplier and a distributor have a Deal stating that they will split the revenue of a certain product 70/30, Cellmobs can automatically calculate these splits and represent them in a report. This takes the complexity out of revenue sharing and ensures all parties are compensated correctly.

Cellmobs' ability to generate these reports not only provides businesses with valuable insights but also brings a high level of transparency and accuracy to the financial operations. This efficiency and clarity can significantly enhance decision-making and business relationships.

## Deals

Deals within Cellmobs can cater to complex revenue sharing arrangements, accommodating the need for flexible business models and agreements. Here's how these elements play out:

- **Tiered Revenue Sharing:** Cellmobs allows Deals to specify different levels of revenue distribution such as gross, adjusted gross, and net. For instance, a participant might be entitled to a certain percentage of gross revenue, while others might receive a share of the net revenue (i.e., after costs are deducted). This flexibility allows for nuanced agreements that better reflect the roles and contributions of the different parties involved.

- **Pre- and Post-Cost Deductions:** The platform can handle agreements where revenue shares are calculated either before or after certain costs are deducted. This gives organizations the flexibility to account for costs in the manner that best suits their specific business model or agreement. 

- **Advance Payments:** In many cases, suppliers or other parties might receive advance payments as part of their deal. Cellmobs can account for these advance payments in its revenue sharing calculations. For instance, the platform can be configured to first recoup the advance from revenues before distributing the remaining amount according to the specified revenue share percentages.

- **Minimum Guarantees:** If a deal includes a minimum guarantee to a supplier or another party, Cellmobs can incorporate this into its revenue sharing reports. For example, if a supplier is guaranteed a minimum revenue share regardless of actual sales, the platform can ensure this amount is paid out first, with any remaining revenue then distributed according to the agreed percentages.


<br><br>