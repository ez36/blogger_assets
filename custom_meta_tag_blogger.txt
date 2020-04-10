<meta content='width=device-width, initial-scale=1' name='viewport'/>
<b:include data='blog' name='all-head-content'/>
<include expiration='7d' path='*.css'/>
<include expiration='7d' path='*.js'/>
<include expiration='3d' path='*.gif'/>
<include expiration='3d' path='*.jpeg'/>
<include expiration='3d' path='*.jpg'/>
<include expiration='3d' path='*.png'/>
<!-- Title -->
<b:if cond='data:view.isHomepage'>
	<title><data:blog.pageTitle/></title>
<b:elseif cond='data:view.isSingleItem'/>
	<title><data:blog.pageName/> - <data:blog.title/></title>
<b:elseif cond='data:view.isMultipleItems and !data:view.isArchive'/>
	<title>
    <b:switch var='data:blog.locale'><b:case value='id'/>Semua Postingan - <data:blog.title/><b:default/>All Posts - <data:blog.title/>
    </b:switch>
    </title>
<b:elseif cond='data:view.isError'/>
	<title> 
    <b:switch var='data:blog.locale'><b:case value='id'/>
    Halaman tidak ditemukan - <data:blog.title/><b:default/>Page Not Found - <data:blog.title/>
    </b:switch>
    </title>
<b:else/>
	<title><data:blog.pageName/></title>
</b:if>
<!-- Meta keywords otomatis homepage, static page, dan post -->
<b:if cond='data:view.isHomepage'>
	<meta expr:content='data:blog.title' name='keywords'/> 
<b:elseif cond='data:view.isSingleItem'/>
	<meta expr:content='data:blog.pageName' name='keywords'/>
</b:if>
<!-- Facebook Meta Tag Open Graph -->
<b:if cond='data:view.isHomepage'>
<b:if cond='data:view.isPost'>
<b:if cond='data:view.isPage'>
<b:if cond='data:blog.url'>
<meta expr:content='data:blog.url' property='og:url'/>
</b:if>
<meta expr:content='data:blog.title' property='og:site_name'/>
<b:if cond='data:blog.pageName'>
<meta expr:content='data:blog.pageName' property='og:title'/>
</b:if></b:if></b:if></b:if>
<meta content='blog' property='og:type'/>
<b:if cond='data:blog.postImageUrl'>
<meta expr:content='data:blog.postImageUrl' property='og:image'/>
<b:else/>
<b:if cond='data:blog.postImageThumbnailUrl'>
<meta expr:content='data:blog.postThumbnailUrl' property='og:image'/>
<b:else/>
<meta content='https://1.bp.blogspot.com/-qBbkyrJhvF4/Xl9My09qVJI/AAAAAAAAG-M/FRcKIlf9kEMJ6ZxK7EB0SrcsaDoX2c0iwCLcBGAsYHQ/s1600/Wahib_NET.jpg' property='og:image'/>
</b:if></b:if>
<b:if cond='data:blog.metaDescription'>
<meta expr:content='data:blog.metaDescription' property='og:description'/>
<b:else/>
<meta expr:content='data:post.snippet' property='og:description'/>
</b:if>
<!-- Remove Duplicate Content-->
<link href='https://www.blogger.com/openid-server.g' rel='openid.server'/>
<link expr:href='data:blog.homepageUrl' rel='openid.delegate'/>
<link expr:href='data:blog.url' rel='canonical'/>
<b:if cond='data:view.isArchive or data:view.isSearch or data:view.isLabelSearch or data:view.isError'>
<meta content='noindex,nofollow' name='robots'/>
</b:if>
<!-- Meta Tag Wahib.NET -->
<meta content='website' property='og:type'/>
<meta content='blogger' name='generator'/>
<meta expr:content='data:blog.title' property='og:site_name'/>
<meta content='https://www.facebook.com/wahibirawan' property='article:author'/>
<meta content='https://www.facebook.com/wahibirawanofficial' property='article:publisher'/>
<meta content='100006394686698' property='fb:admins'/>
<meta content='417333228693312' property='fb:app_id'/>
<meta content='1453094381626648' property='fb:pages'/>
<meta content='id_ID' property='og:locale'/>
<meta content='en_GB' property='og:locale:alternate'/>
<meta content='en_US' property='og:locale:alternate'/>
<meta content='id' name='geo.country'/>
<meta content='Indonesia' name='geo.placename'/>
<meta content='Wahib Irawan' name='Author'/>
<meta content='#332D4F' name='msapplication-navbutton-color'/>
<meta content='#332D4F' name='apple-mobile-web-app-status-bar-style'/>
<meta content='#332D4F' name='theme-color'/> 
<meta content='general' name='rating'/>
<!-- Twitter Meta Tag -->
  <meta content='summary_large_image' name='twitter:card'/>
  <meta expr:content='data:blog.pageTitle' name='twitter:title'/>
  <meta content='@wahiblicious' name='twitter:site'/>
  <b:if cond='data:blog.metaDescription'>
    <meta expr:content='data:blog.metaDescription' name='twitter:description'/>
    <b:else/>
    <meta expr:content='data:blog.title' name='twitter:description'/>
  </b:if>
  <b:if cond='data:blog.postImageUrl'>
    <meta expr:content='data:blog.postImageUrl' name='twitter:image'/>
    <meta expr:content='data:blog.pageName' name='twitter:image:alt'/>
    <b:else/>
    <b:if cond='data:blog.postImageThumbnailUrl'>
      <meta expr:content='data:blog.postThumbnailUrl' name='twitter:image'/>
      <meta expr:content='data:blog.pageName' name='twitter:image:alt'/>
      <b:else/>
      <meta content='https://1.bp.blogspot.com/-qBbkyrJhvF4/Xl9My09qVJI/AAAAAAAAG-M/FRcKIlf9kEMJ6ZxK7EB0SrcsaDoX2c0iwCLcBGAsYHQ/s1600/Wahib_NET.jpg' name='twitter:image'/>
    </b:if></b:if>
<!-- JavaScript -->
<script type='application/ld+json'>{ &quot;@context&quot;: &quot;http://schema.org&quot;, &quot;@type&quot;: &quot;WebSite&quot;, &quot;url&quot;: &quot;<data:blog.homepageUrl/>&quot;, &quot;potentialAction&quot;: { &quot;@type&quot;: &quot;SearchAction&quot;, &quot;target&quot;: &quot;<data:blog.homepageUrl/>?q={search_term}&quot;, &quot;query-input&quot;: &quot;required name=search_term&quot; } }</script>
