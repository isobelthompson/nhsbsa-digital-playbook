---
layout: page
title: "table test"
description:
status: DRAFT
tags: [data-viz, data-viz-colour]
order:
    data-viz: 2
    data-viz-colour: 3
---

// defaults
var md = require('markdown-it')()
            .use(require('markdown-it-multimd-table'));

// full options list (equivalent to defaults)
var md = require('markdown-it')()
            .use(require('markdown-it-multimd-table'), {
              multiline:  false,
              rowspan:    false,
              headerless: false,
              multibody:  true,
              autolabel:  true,
            });

md.render(/*...*/)