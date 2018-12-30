---
layout: post
title: Immutable data part 1
---

A lot of data science platforms seem to assume that incoming data can be treated as a stream of immutable items. In computer science, a data item is **immutable** if it never changes once it is created. For example, when a customer completes a purchase, the data created by the transaction is immutable. (If the transaction is later cancelled, say because an item was returned, the return can simply be treated as a separate transaction.) This assumption makes the design of a platform for studying company data much easier, because you can think of the business’ processes as contributing to an ever-increasing data set. 

But what if you want to study data that is not immutable? For example, at Bloomberg Law one of the main sets of legal documents we deal with is court dockets. A court docket describes the day-by-day events that take place in a court case. While the events in the case, that are listed as dated entries in the docket, are mostly immutable, the case’s list of parties and the attorneys representing them changes over time, as attorneys are added or terminated, and even as parties themselves are added or removed.

Over the next few posts I want to identify some other examples of data sets containing non-immutable data items, and also discuss strategies for handling them.