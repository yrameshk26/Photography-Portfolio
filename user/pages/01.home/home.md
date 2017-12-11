---
title: 'Ramesh Yoha'
images:
    -
        title: 'Vinayahar Statue'
        thumbnail: 01.jpg
        description: 'Hindu Lorn Vinayahar Under The Sacred Tree In An Autism School Located At Dehiwela.'
    -
        title: 'Red Fox Of Algonquin Park'
        thumbnail: 02.jpg
        description: 'Harmless Red Fox Of Algonquin Park Which Is 2 Hour Away From Toronto.'
    -
        title: 'Halloween Pumpkins'
        thumbnail: 03.jpg
        description: 'Large Orange Pumpkins In A Home Garden Store At Syracuse,NY.'
    #-
    #    title: 'Lux Parade Girls'
    #    thumbnail: 04.jpg
    #    description: 'Srilankan Pretty Girls Going On A Parade Near Independence Square Arcade.'
    -
        title: 'Mom''s Love'
        thumbnail: 005.jpg
        description: 'A Mom Crow Feeding Its Kid On The Early Morning, At Wellawatte Beach.'
    -
        title: 'Silky Water'
        thumbnail: 06.jpg
        description: 'Soothing Water Stream At Chittagong Falls, NY.'
    #-
    #    title: 'Old Architecture - Syracuse'
    #    thumbnail: 07.jpg
    #    description: 'Old Architecture of Syracuse City, New York.'
    -
        title: 'Ring-Billed Gull'
        thumbnail: 08.jpg
        description: 'Ring-Billed Gull of Staten Island - Easily Spotted From The Ferry To Staten Island.'
    -
        title: 'Early Morning Walk'
        thumbnail: 09.jpg
        description: 'What A Way To Start Walking Early In The Morning With The Rising Sun at Arugambay.'
    -
        title: 'Misty Morning'
        thumbnail: 10.jpg
        description: 'Early Morning Mist While On Our Way To Algonquin Trails.'
    #-
    #    title: 'Nature''s Reflection'
    #    thumbnail: 11.jpg
    #    description: 'Nature''s Reflections Are Always Pleasing To Eyes, At The Algonquin Trails.'
    -
        title: 'Symmetry Of Brooklyn Bridge'
        thumbnail: 12.jpg
        description: 'Symmetrical View Of Brooklyn Bridge, New York.'
    #-
    #    title: 'Parking Meter'
    #    thumbnail: 13.jpg
    #    description: 'Old Type Parking Meter Located At Syracuse New York'
    #-    
    #    title: 'Apple Cider Gin'
    #    thumbnail: 14.jpg
    #    description: 'Apple Cider Gins Of Syracuse Winery Farms.'
    -
        title: 'Wrong Turn'
        thumbnail: 15.jpg
        description: 'Haunted Looking House On A Remote Location Near Chittagong Falls.'
    #-
    #    title: 'Badminton Birdie'
    #    thumbnail: 16.jpg
    #    description: 'Close Up Of Shuttle Cock - Mobile Phone (Google Pixel) Photography.'
    -
        title: 'Newyork Buildings'
        thumbnail: 17.jpg
        description: 'Morning View Of Beautiful Newyork City''s Buildings.'
    -
        title: 'Shri Swamy Narayan Mandir'
        thumbnail: 18.jpg
        description: 'Fascinating Look Of Shri Swamy Narayan Mandir Located At Brampton.'
    #-
    #    title: 'Hay Fields'
    #    thumbnail: 19.jpg
    #    description: 'Yellow Hay Fields on a Nice Sunny Day, Near Pickering.'
    #-
    #    title: 'Snow Flakes'
    #    thumbnail: 20.jpg
    #    description: 'Macro View Of Snow Flakes After a Heavy Snow Fall.'
    #-
    #    title: 'Top View Of Algonquin Trail'
    #    thumbnail: 21.jpg
    #    description: 'Pleasing View Of Nature After A Long Hike At Algonquin Park.'
    #-
    #    title: 'Stone Balancing & Breaking'
    #    thumbnail: 22.jpg
    #    description: 'Stone Balancing & Breaking Near A River, While Relaxing On A Mid Of A Hike, Algonquin Trails.'
    -
        title: 'Brunch At Cinnamon Grand'
        thumbnail: 23.jpg
        description: 'Healthy Selection Of Food At Taprobane Restaurant Of Cinnamon Grand Hotel, Colombo'
    -    
        title: 'Wedding Season'
        thumbnail: 24.jpg
        description: 'Groom Getting Ready For The Big Day, At A Srilankan Christian Wedding.'
    #-
    #    title: 'Virgin Mojito'
    #    thumbnail: 25.jpg
    #    description: 'Virgin Mojito Mocktail From "The Barnesbury", Colombo.'
    #-
    #    title: 'White Hair Falls'
    #    thumbnail: 26.jpg
    #    description: 'Relaxing View Of Chittagong Water Falls At New York State.'
    -
        title: 'Ponnambala Vaneshwarar'
        thumbnail: 27.jpg
        description: 'Lord Shiva''s Ponnambala Vaneshwarar Temple At Heart Of The Colombo City.'
    #-
    #    title: 'Cinnamon Desserts'
    #    thumbnail: 28.jpg
    #    description: 'Its Not Just Tastes Good, But Looks Good Too, At Taprobane - Cinnamon Grand.'

form:
    action: /
    name: contact-form
    fields:
        -
            name: name
            label: Name
            placeholder: Name
            type: text
            validate:
                required: true
        -
            name: email
            label: Email
            placeholder: Email
            type: email
            validate:
                required: true
        -
            name: message
            label: Message
            placeholder: Message
            type: textarea
            rows: 4
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Send
            classes: special
        -
            type: reset
            value: Reset
    process:
        -
            email:
                from: '{{ config.plugins.email.from }}'
                to: ['{{ config.plugins.email.to }}']
                subject: 'Ramesh Yoha 👁️ Photography 📸 Portfolio 🌍 : Message from {{ form.value.name|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            display: /thank-you
---
