---
layout: post
title:  "2023 Week 16 Week Retro"
date:   2023-04-23 09:17:19 +0100
categories: update
---
# What I'm up to

- AWS accounts management
- Code quality improvement

During my Terraform work, I encountered an issue upon upgrading one of the workspaces from Terraform 0.11 to 1.4.4. The problem arose when Terraform complained about the usage of an unordered set to create multiple modules via the "count" meta-parameter. After discussing the issue, we decided to use "for_each" instead of count to ensure name uniqueness and avoid reshuffling of items that occurs with unordered lists.

To handle object renaming in Terraform state (since I am currently on the 0.11->0.12 stage where "moved" blocks are not available yet), I use Python scripting to hack the Terraform state and rename objects. This is necessary for multiple workspaces with thousands of objects.  The "Allow empty apply" feature in TFE is extremely useful when upgrading a workspace and performing a mandatory apply.
