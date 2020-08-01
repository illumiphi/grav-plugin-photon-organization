% name: Organization
% def: post_date=$(date +%Y-%m-%d)
% def: author='/about'
% def: collection_name='Articles'
---
title: ${title}
subtitle: ${subtitle}
date: ${post_date}
author: ${author}
sets:
    default:
        name: ${collection_name}
        showCount: true
        showMenu: true
    members:
        name: Members
        showCount: false
        showMenu: false
content:
    items: '@self.children'
members:
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'person'
events:
    items: 
        '@taxonomy.category': ${category}
    filter:
        type: 'event'
posts:
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

