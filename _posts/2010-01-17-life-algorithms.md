---
title: 生活中的各种算法
layout: post
category: geek生活
---

## 从哪里开始工作 ##

    event = select_event(event_list)
    next_step = pick_point(event)

    while (next_step != null && may_continue){
        do(next_step)
        next_step ++
    }

    save_point(event, next_step)

## 怎样发现自己最喜欢的事 ##

    happiness[] = pick_happy(memory_list)

    for event in happiness
        happy_reasons = why_happy(event)
        reason_list.append(happy_reasons)

    for i from 0 to len(reason_list) -1
        r = reason_list[i]
        statistics[r] = 1
        for j from i+1 to len(reason_list) -1
            if reason_list[j] == r
                statistics[r] += 1
        reason_list.remove(r)

    sort(statistics)
    favorite_things = pick_head(statistics)

## 怎样读文献 ##

    if irrelevant(title)
        return
    work = read( abstract )
    if not interesting(work)
        return

    if is_measurement( work )
        for c in conclusions
            if is_doubtful(c)
                c.where = read( outline, figs, tables)
                check(c)
            if is_useful(c)
                save(c)
    if problem_oriented( work)
        hard_points = think(abstract, outline, figs, tables)
        for p in hard_points
            p.content = read( p.where )
            if is_useful( p.content )
                save(p.content)
        drawbacks = summary()
        save( drawbacks )
    if is_good(paper)
        (wrong_sentences, useful_sentences) = read_through(paper)
        save(useful_sentences)
        save(wrong_sentences)
