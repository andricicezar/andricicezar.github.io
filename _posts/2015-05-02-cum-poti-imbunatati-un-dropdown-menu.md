---
id: 10
title: 'Cum poti imbunatati un dropdown menu?'
date: '2015-05-02T13:06:01+03:00'
author: 'Cezar Andrici'
layout: single
guid: '/?p=10'
permalink: /cum-poti-imbunatati-un-dropdown-menu/
categories:
    - 'Imbunatatire UX'
tags:
    - 'dropdown cu subcategorii'
    - 'dropdown menu'
    - 'meniu dropdown'
---

Daca ai pe site un dropdown menu cu subcategorii, sunt sanse foarte mari sa ai problema asta de UX.

[![Bootstrap Bug](/wp-content/uploads/2015/04/bootstrap-bug.gif)](/wp-content/uploads/2015/04/bootstrap-bug.gif)

Cea mai folosita solutie e adaugarea unui mic delay, dar in acest caz navigarea prin meniu devine lenta. Poate parea o problema nesemnificativa, in schimb solutia e foarte foarte simpla si merita implementata. Si solutia este:

[![Solutie Meniu](/wp-content/uploads/2015/04/screen_shot_2013-03-06_at_1.17.35_am.png)](/wp-content/uploads/2015/04/screen_shot_2013-03-06_at_1.17.35_am.png)

Simplu huh? La fiecare miscare se calculeaza un triunghi cu colturile meniului si cat timp cursorul nu iese din triunghi, nimic nu se schimba. Simplu, si functioneaza perfect.

Din fericire, [exista o librarie](https://github.com/kamens/jQuery-menu-aim) super usor de integrat si care functioneaza doar prin adaugarea unei linii de cod. Daca vreti sa vedeti cum functioneaza, am folosit-o la meniul de la [incarcari.ro](http://incarcari.ro) si am scapat de problema.

*Aveti alte solutii la problema asta? :D*