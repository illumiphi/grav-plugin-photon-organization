% name: Organization
% def: post_date=$(date +%Y-%m-%d)
% def: author='/about'
% def: collection_name='Articles'
---
title: ${title}
subtitle: ${subtitle}
date: ${post_date}
author: ${author}
content:
    title: Articles
    items: '@self.children'
members:
    title: Members
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'person'
events:
    title: Upcoming Events
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'event'
posts:
    title: Recent Posts
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'post'
taxonomy:
    category:
        - organization
    tag:
data:
    organization:
        '@type': Organization
        name: ${org_name}
        telephone: ${org_phone}
        url: ${org_url}
        location:
            address:
                streetAddress: ${org_street}
                addressLocality: ${org_city}
                addressRegion: ${org_state}
                postalCode: ${org_zip}
                addressCountry: ${org_country}
---

${summary}

===

