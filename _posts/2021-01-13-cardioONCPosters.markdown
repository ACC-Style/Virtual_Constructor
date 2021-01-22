---
title:  "Cardio Onc Poster with star flags"
date:   2021-01-15 10:14:44 -0500
categories: icons
---
<div class="ul_none">
{% for item in site.data.CARDIOONC %}
<article  class="c_black m-b_4 m-b_5:md m-t_5 p-t_4 max-w_30">
    <div class="br_1 br_radius br_solid br_black-2 flex flex_column flex_column:lg flex_row:md font_ui h:bg_black-2 m-x_n2 relative m-t_4" style="height: 100%">  
        <div class="display_none:lg flex_none justify_center p-l_4:md p-y_3" style="width: 4rem">
            {% if item.featured == "true"  %}
            <div class="absolute t_n3 r_4">
                <i class="c_highlight-1 fa-bookmark fas font_10 relative text-shadow_black-1 z_5"></i>
                <span class="absolute font_bold l_0 lh_0 vertical-align_middle font_n2 uppercase m-t_1 m_auto r_0 t_3 text_center z_5"><i class="c_black-8 fa-star fas font_2 text-shadow_white-n1"></i></span>
            </div>
            {% endif %}
            <div class="flex_none m-t_n5 m_auto m_auto:md self_center text_center" style="width: 3rem">
                <div class="pathwayColor{ bg_primary } flex_shrink relative aspect_1x1 shadow_3 text_center texture_ondemand thumb [ bg-blend_multiply bg_center bg_contain bg_no-repeat  ][ br_2 br_black-3 br_radius br_solid ]">
                    <div class="absolute b_0 flex h:opacity justify_center l_0 opacity_7 r_0 self_center t_0 text_center w_100"><em class="absolute c_white-9 fa-user-chart fas flex_auto font_2 self_center text_center w_100"></em></div>
                </div>
            </div>
        </div>
        <div class="block:lg display_none m-t_n5 m-x_5 p-x_5 relative">
            {% if item.featured == "true"  %}
            <div class="absolute t_n3 r_5 m-r_4">
                <i class="c_highlight-1 fa-bookmark fas font_10 relative text-shadow_black-1 z_5"></i>
                <span class="absolute font_bold l_0 lh_0 vertical-align_middle font_n2 uppercase m-t_1 m_auto r_0 t_3 text_center z_5"><i class="c_black-8 fa-star fas font_2 text-shadow_white-n1"></i></span>
            </div>
            {% endif %}
            <div class="m-t_n5 m_auto m_auto:md self_center text_center">
                <div class="aspect_21x9 bg-blend_overlay bg_cover bg_no-repeat bg_primary br_2 br_radius br_solid br_black-3 flex_shrink relative shadow_3 texture_ondemand text_center thumb">
                    <div class="absolute b_0 flex h:opacity justify_center l_0 opacity_7 r_0 self_center t_0 text_center w_100">
                    <em class="absolute c_white-9 fa-user-chart fas flex_auto font_5 self_center text_center w_100"></em>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex_auto [ c_primary-n4  font_0 font_1:md font_copy font_regular lh_2 ][ p-b_3 p-b_4:md p-l_0:lg p-l_4:md ">
            <div class="p-t_2 p_4  p-y_0 p-y_3:md p-x_5:lg">
                <a class="expanded-click-area h:undecorated p-b_3" target="_blank" href="{{ item.videolink }}">{{item.title}}</a>
            </div>
        </div>
    </div>
    <div class="c_black flex flex_wrap font_n2 justify_between m-t_2 p-t_2">
        <div class="flex_shrink block font_bold text_left p-r_3 m-r_3 br-r_1 br_black-3 br_solid">
<a href="{{ item.pdflink }}" class="block h:underline uppercase" target="_blank"><em class="far fa-paperclip"></em> Attachments</a>
        </div>
        <div class="flex_grow uppercase text_right">
        {% assign credits = item.credits %}
        {% if credits.size > 0 %}
        {% include credits.html %}
        {%  endif %}
        </div>
    </div>
</article>
{% endfor %}
</div>
