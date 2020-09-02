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
    showCount: true
    showMenu: true
    items: '@self.children'
members:
    title: Members
    showCount: true
    showMenu: true
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'person'
events:
    title: Upcoming Events
    showCount: true
    showMenu: true
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'event'
posts:
    title: Recent Posts
    showCount: true
    showMenu: true
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'post'
taxonomy:
    category:
        - ${category}
    tag:
        - ${tag}
show_gallery: false
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

