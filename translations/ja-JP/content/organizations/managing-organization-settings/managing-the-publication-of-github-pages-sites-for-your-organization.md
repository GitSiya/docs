---
title: Organization の GitHub Pages サイトの公開を管理する
intro: 'Organization のメンバーが Organization 内のリポジトリから {% data variables.product.prodname_pages %} サイトを公開できるかどうかを制御し{% ifversion ghec %}、メンバーがサイトに対して選択できる可視性を制限できます{% endif %}。'
permissions: 'Organization owners can manage the publication of {% data variables.product.prodname_pages %} sites from repositories in the organization.'
product: '{% data reusables.gated-features.pages %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
redirect_from:
  - /github/setting-up-and-managing-organizations-and-teams/disabling-publication-of-github-pages-sites-for-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/managing-the-publication-of-github-pages-sites-for-your-organization
topics:
  - Organizations
  - Teams
shortTitle: Pagesのサイトの公開管理
---

{% ifversion fpt %}
You can choose to allow or disallow organization members from publishing {% data variables.product.prodname_pages %} sites. Organizations that use {% data variables.product.prodname_ghe_cloud %} can also choose to allow publicly published sites, privately published sites, both, or neither. 詳しい情報については[{% data variables.product.prodname_ghe_cloud %}のドキュメンテーション](/enterprise-cloud@latest/organizations/managing-organization-settings/managing-the-publication-of-github-pages-sites-for-your-organization)を参照してください。
{% elsif ghec %}
You can choose to allow organization members to create publicly published sites, privately published sites, both, or neither. {% data variables.product.prodname_pages %} サイトのアクセス制御の詳細については、「[{% data variables.product.prodname_pages %} サイトの可視性を変更する](/pages/getting-started-with-github-pages/changing-the-visibility-of-your-github-pages-site)」を参照してください。
{% endif %}

{% data variables.product.prodname_pages %} サイトの公開を許可しない場合、すでに公開されているサイトはすべて公開されたままになります。 そのサイトは手動で取り下げることができます。 詳細は「[{% data variables.product.prodname_pages %}サイトの取り下げ](/pages/getting-started-with-github-pages/unpublishing-a-github-pages-site)」を参照してください。

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.member-privileges %}{% ifversion fpt %}
1. Under "Pages creation, select or deselect **Public**.

   ![Checkboxes to allow or disallow creation of {% data variables.product.prodname_pages %} sites](/assets/images/help/organizations/github-pages-creation-checkboxes-fpt.png){% elsif ghec %}
1. [Pages creation] で、許可する可視性を選択し、禁止する可視性を選択解除します。

   ![Checkboxes to allow or disallow creation of {% data variables.product.prodname_pages %} sites](/assets/images/help/organizations/github-pages-creation-checkboxes.png){% else %}
1. [Pages creation] で、[**Allow members to publish sites**] を選択または選択解除します。

   ![[Allow members to publish sites] オプションの [Unselected] チェックボックス](/assets/images/help/organizations/org-settings-pages-disable-publication-checkbox.png){% endif %}{% ifversion fpt or ghec %}

   {% indented_data_reference reusables.pages.privately-publish-ghec-only spaces=3%}{% endif %}

1. [**Save**] をクリックします。

## 参考リンク

- 「[{% data variables.product.prodname_pages %} について](/pages/getting-started-with-github-pages/about-github-pages)」
