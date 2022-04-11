<script setup>
import facebookIcon from "@/assets/Social/facebook.svg";
import instagramIcon from "@/assets/Social/instagramm.svg";
import vkIcon from "@/assets/Social/vk.svg";
import youtubeIcon from "@/assets/Social/youtube.svg";
</script>

<template>
  <div class="social">
    <h3>Мы в соцсетях</h3>
    <div>
      <a
        href="https://www.facebook.com/business/news?campaign_id=1635645059&extra_1=s|c|313664562371|e|facebook%27|&placement=&creative=313664562371&keyword=facebook%27&partner_id=googlesem&extra_2=campaignid%3D1635645059%26adgroupid%3D61926940465%26matchtype%3De%26network%3Dg%26source%3Dnotmobile%26search_or_content%3Ds%26device%3Dc%26devicemodel%3D%26adposition%3D%26target%3D%26targetid%3Dkwd-362360550869%26loc_physical_ms%3D1009827%26loc_interest_ms%3D%26feeditemid%3D%26param1%3D%26param2%3D&gclid=CjwKCAiAprGRBhBgEiwANJEY7PBh5CNU-DMM2ryfKGwJFP-QbkXS-o8kjV8eCD7VJdpMyxA96psV_hoCwjAQAvD_BwE"
      >
        <img :src="facebookIcon" alt="" />
      </a>
      <a href="https://www.instagram.com/nozhiman/">
        <img :src="instagramIcon" alt="" />
      </a>
      <a
        href="https://vk.com/login?u=2&to=/login?op=logout&hash=1647115811_fa0b3f130f1b3be9c1&rnd=161945119"
      >
        <img :src="vkIcon" alt="" />
      </a>
      <a href="https://www.youtube.com/channel/UCjU8SRkq31qdAgZx54iKvYw">
        <img :src="youtubeIcon" alt="" />
      </a>
    </div>
  </div>
</template>

<style>
.social {
  display: flex;
  align-items: center;
  margin-top: 40px;
}
.social a {
  margin: 0 7px;
  align-items: center;
}
.social div {
  padding: 0 20px;
}
@media screen and (max-width: 376px) {
  .social {
    margin-bottom: 20px;
  }
}
</style>
