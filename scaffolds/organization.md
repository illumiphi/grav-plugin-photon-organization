% name: Post
% folder: date
% def: author='/about'
% def: post_date=$(date +%Y-%m-%d)
% def: collection_name='Articles'
---
title: ${title}
subtitle: ${subtitle}
author: ${author:-/about}
collection:
    name: ${collection_name:-Articles}
    showCount: true
    showMenu: true
content:
    items: '@self.children'
child_type: article
taxonomy:
    category: 
        - ${category}
    tag: 
        - ${tag}
show_gallery: false
data:
    organization:
        '@type': Organization
        name: ${org_name:-$title}
        telephone: ${org_phone}
        url: ${org_url} 
        location:
            address:
                streetAddress: ${org_street}
                addressLocality: ${org_city}
                addressRegion: ${org_state:-OR}
                postalCode: ${org_zip}
                addressCountry: ${org_country}
---

${summary}

===

