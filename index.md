---
layout: page
title: Dan's Workspace
description: "Dan's Workspace"
---
{% include JB/setup %}

<table width="100%" rowspan="0" colspan="0">
<tr>
<td width="70%">
    <div class="home-page-content">
        {% for post in site.posts limit:10 %}
            <div class="home-page-post">
                <div class="post-header">
                    <div class="date">{{ post.date | date_to_string }}</div>
                    <div class="tags"> 
                        <label>Tags: </label>{{ post.tags | array_to_sentence_string }}
                    </div>
                    <div class="category">
                        <label>Category: </label>
                        <span>{{ post.category }}</span>
                    </div>
                </div>
                <div class="post-content">
                    <div class="title"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></div>
                    <div class="abstract">{{ post.description | markdownify }}</div>
                    <div style="float:right;"><a href="{{ BASE_PATH }}{{ post.url }}">Read more</a></div>
                </div>
                {% if forloop.index != 5 %}
                    <div class="post-footer">&nbsp;</div>
                {% endif %}
            </div>
        {% endfor %}
    </div>
</td>

<td width="30%" style="vertical-align:top;">
    <div class="home-page-sidebar">
        <ul id="social_link" class="clearfix">
            <li class="weibo_button">
                <a class="target_blank" href="http://weibo.com/danshan" target="_blank">rss</a>
            </li>
            <li class="rss_button">
                <a class="target_blank" href="/atom.xml" target="_blank">rss</a>
            </li>
            <li class="twitter_button">
                <a class="target_blank" href="https://twitter.com/shanhh" target="_blank">twitter</a>
            </li>
        </ul>
        <div class="sidebar-title">文章分类</div>
        <div>
            <ul class="tag_box inline">
                {% assign categories_list = site.categories %}
                {% include JB/categories_list %}
            </ul>
        </div>
        <br>
        <div class="sidebar-title">标签</div>
        <div>
            <ul class="tag_box inline">
                {% assign tags_list = site.tags %}  
                {% include JB/tags_list %}
            </ul>
        </div>
        <br>
        <div class="sidebar-title">Bitbucket Repositories</div>
        <div>
            <ul class="tag_box">
                <li><a class="btn btn-small" target="_blank" href="https://bitbucket.org/danshan/dseverything">dseverything</a></li>
                <li><a class="btn btn-small" target="_blank" href="https://bitbucket.org/danshan/blackberry_google_talk">blackberry gtalk</a></li>
                <li><a class="btn btn-small" target="_blank" href="https://bitbucket.org/danshan/blackberry_simple_md5_tools">blackberry md5 tools</a></li>
                <li><a class="btn btn-small" target="_blank" href="https://bitbucket.org/danshan/blog">blog</a></li>
            </ul> 
        </div>
    </div>
</td>
</tr>
</table>
<hr>
<div style="width:50%;margin-left:auto;margin-right:auto;text-align:center;clear:both;">
	<a href="/archive.html">查看所有{{site.posts.size}}篇文章...</a>
</div>



