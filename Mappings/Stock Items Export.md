***Stock Items Export***
<p>Status: Completed</p>
<table>
<tbody>
<tr>
<th>Version</th>
<th>Description</th>
<th>Status</th></tr>
<tr>
<td>1.0</td>
<td>Development completed for M1</td>
<td>Completed</td></tr></tbody></table>
<p>Table of Content</p>
<p><ac:structured-macro ac:macro-id="dd2f8854-9b46-4e89-978c-fb4db514818a" ac:name="toc" ac:schema-version="1" /></p>
<h2>Acumatica Stock Item Field Mapping with WooCommerce Product fields</h2>
<table>
<tbody>
<tr>
<td class="highlight-grey" colspan="7" data-highlight-colour="grey" style="text-align: center;"><strong>Acumatica (Source)</strong></td>
<td class="highlight-grey" colspan="3" data-highlight-colour="grey"><strong>WooCommerce (Target)</strong></td></tr>
<tr>
<td class="highlight-grey" data-highlight-colour="grey"><strong>Field Name</strong></td>
<td class="highlight-grey" colspan="1" data-highlight-colour="grey"><strong>Acumatica Path</strong></td>
<td class="highlight-grey" colspan="1" data-highlight-colour="grey"><strong>Mandatory</strong></td>
<td class="highlight-grey" data-highlight-colour="grey"><strong>Column Name</strong></td>
<td class="highlight-grey" colspan="1" data-highlight-colour="grey"><strong>Data Access Class</strong></td>
<td class="highlight-grey" data-highlight-colour="grey"><strong>Framework</strong></td>
<td class="highlight-grey" data-highlight-colour="grey"><strong>Comment <span style="color: rgb(68,68,68);">(Acu-&gt;Woo)</span></strong></td>
<td class="highlight-grey" data-highlight-colour="grey"><strong>Field Name</strong></td>
<td class="highlight-grey" data-highlight-colour="grey"><strong>Value Example</strong></td>
<td class="highlight-grey" colspan="1" data-highlight-colour="grey"><strong>WC Path</strong></td></tr>
<tr>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td colspan="1" style="text-align: center;">Y</td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td>&nbsp;</td>
<td>Product ID is generated by WooCommerce</td>
<td>id</td>
<td>794</td>
<td colspan="1">Not visible in the interface</td></tr>
<tr>
<td>Description</td>
<td colspan="1"><span>Stock Items&gt;Description</span></td>
<td colspan="1" style="text-align: center;">Y</td>
<td>Descr</td>
<td colspan="1"><span>InventoryItem</span></td>
<td>&nbsp;</td>
<td>Description in Summary area</td>
<td>name</td>
<td>Premium Quality</td>
<td colspan="1">Products-&gt; Product Name</td></tr>
<tr>
<td>Stock Item</td>
<td colspan="1"><span>Stock Items&gt;General Settings&gt;Item Class</span></td>
<td colspan="1" style="text-align: center;">Y</td>
<td>StkItem</td>
<td colspan="1">INItemClass</td>
<td>Stock Items&gt;Item Class</td>
<td>
<p>In ItemClass-&gt; Stock item Boolean= True AND Item type = Finished Good -&gt; In WooCom Product type = simple product</p>
<p><em>{In M1 consider only simple products in WooCommerce}</em></p></td>
<td><span>type</span></td>
<td>simple</td>
<td colspan="1">Products-&gt; Product Data</td></tr>
<tr>
<td>ItemStatus</td>
<td colspan="1"><span>Stock Items&gt;ItemStatus</span></td>
<td colspan="1" style="text-align: center;">Y</td>
<td><span>ItemStatus</span></td>
<td colspan="1">InventoryItem</td>
<td>Stock Items&gt;ItemStatus</td>
<td>
<ul>
<li>If Acumatica Status = Active -&gt; In WC Status = Published</li>
<li>If Acumatica Status = Inactive/No Sale/No Purchases/ No Request/ Marked for deletion -&gt; In WC Status = Draft<br /><em>{WooCommerce &quot;Pending Review&quot; status not considering}</em></li></ul>
<p><strong><em>&lt;Clarification- QA&gt;</em></strong></p>
<p><em>The Availability is depend with the status of the product? What would be the relationship between the status with availability and the visibility.</em></p>
<p><em>&lt;Please refer <ac:link><ri:page ri:content-title="Stock Item Entity" /></ac:link>&gt;</em></p></td>
<td>status</td>
<td>publish</td>
<td colspan="1">Products-&gt; Publish-&gt; Status</td></tr>
<tr>
<td>Visibility</td>
<td colspan="1"><span>Stock Items&gt;Ecommerce&gt;Visibility</span></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td>Visibility</td>
<td colspan="1">InventoryItem</td>
<td>Stock Items&gt;Visibility</td>
<td>
<p><span>In Acumatica Visibility = Visible-&gt; In WC <span>Catalog</span><span> visibility</span> = <span style="color: rgb(60,67,74);">Shop and search results</span></span></p>
<p>In Acumatica Visibility = Featured -&gt; In WC <span>Catalog</span><span> visibility</span><span> = </span><span style="color: rgb(60,67,74);">Shop and search results AND </span>Featured Boolean = True</p>
<p><span>In Acumatica Visibility = Invisible-&gt; In WC Catalog visibility = Hidden</span></p></td>
<td>featured</td>
<td>FALSE</td>
<td colspan="1">Product-&gt; Publish</td></tr>
<tr>
<td>Description</td>
<td colspan="1"><span>Stock Items&gt;Description tab&gt;Description</span></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td>Stock Items&gt;Description</td>
<td>&nbsp;</td>
<td>description</td>
<td>&nbsp;</td>
<td colspan="1">Product-&gt; Description</td></tr>
<tr>
<td>Meta Description</td>
<td colspan="1"><span>Stock Items&gt;Ecommerce&gt;Meta Description</span></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td>MetaDescription</td>
<td colspan="1">InventoryItem</td>
<td>Stock Items&gt;Meta Description</td>
<td>&nbsp;</td>
<td>short_description</td>
<td>&nbsp;</td>
<td colspan="1">Product-&gt; Product short description</td></tr>
<tr>
<td>InventoryID</td>
<td colspan="1"><span>Stock Items&gt;Inventory ID</span></td>
<td colspan="1" style="text-align: center;">Y</td>
<td>InventoryCD</td>
<td colspan="1">InventoryItem</td>
<td>Stock Items&gt;Inventory ID</td>
<td>&nbsp;</td>
<td>sku</td>
<td>&nbsp;</td>
<td colspan="1">Product-&gt; Inventory</td></tr>
<tr>
<td>Default Price</td>
<td colspan="1"><span>Stock Items&gt;Price/Cost info&gt;Price Management</span></td>
<td colspan="1" style="text-align: center;">Y</td>
<td>BasePrice</td>
<td colspan="1">InventoryItem</td>
<td>Stock Items&gt;DefaultPrice</td>
<td><em> {M1 Consider only default price}</em></td>
<td>regular_price</td>
<td>21.99</td>
<td colspan="1">Product-&gt; General</td></tr>
<tr>
<td>Stock Item</td>
<td colspan="1"><span>Stock Items&gt;General Settings&gt;Item Class</span></td>
<td colspan="1" style="text-align: center;">Y</td>
<td>StkItem</td>
<td colspan="1"><span>INItemClass</span></td>
<td>Stock Items&gt;Item Class</td>
<td>
<p>In ItemClass-&gt; Stock item Boolean=True means it is a stock item then in WC Virtual Boolean should =False&nbsp;</p>
<p><em>{Virtual items will consider in M2}</em></p></td>
<td>virtual</td>
<td>FALSE</td>
<td colspan="1">Product-&gt; Virtual</td></tr>
<tr>
<td>
<p>&nbsp;</p></td>
<td colspan="1">&nbsp;</td>
<td colspan="1" style="text-align: center;">Y</td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td>&nbsp;</td>
<td><strong><em>[Default value = TAXABLE]</em></strong></td>
<td>tax_status</td>
<td>taxable</td>
<td colspan="1">Product-&gt; General</td></tr>
<tr>
<td><span>Tax Category List</span></td>
<td colspan="1">&nbsp;</td>
<td colspan="1" style="text-align: center;">Y</td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td>&nbsp;</td>
<td>
<p><em>Tax Class can be mapped using the Substitution Lists</em><strong><em><span>. </span></em></strong><em>if not</em></p>
<p><strong><em><span>&nbsp;</span></em></strong><strong><em>[Default value = Standard] </em></strong><em>will apply</em></p></td>
<td><span>tax_class</span></td>
<td>Standard rate</td>
<td colspan="1"><span>Product-&gt; General</span></td></tr>
<tr>
<td>Availability</td>
<td colspan="1">Stock Items&gt;Ecommerce</td>
<td colspan="1">&nbsp;</td>
<td>Availability</td>
<td colspan="1">InventoryItem</td>
<td>Stock Items&gt;Availability</td>
<td>
<ul>
<li>If &quot;Set as Available (Track Qty)&quot; -&gt; In Inventory tab-&gt; Manage Stock Boolean = True</li>
<li>If &quot;Set as Available (Don&rsquo;t Track Qty)&quot; -&gt; In Inventory tab-&gt; Manage Stock Boolean = False<br />{Default value false}</li></ul>[Inventory configuration default value can be setup]</td>
<td>manage_stock</td>
<td>FALSE</td>
<td colspan="1">Product-&gt; Inventory</td></tr>
<tr>
<td><s>Qty.On Hand</s></td>
<td colspan="1"><s>Stock Items&gt;Warehouses</s></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td>&nbsp;</td>
<td><em>{Will be handled in M2 Product Availability entity}</em></td>
<td><s>stock_quantity</s></td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td></tr>
<tr>
<td>Availability</td>
<td colspan="1">Stock Items&gt;Ecommerce</td>
<td colspan="1">&nbsp;</td>
<td>Availability</td>
<td colspan="1">InventoryItem</td>
<td>Stock Items&gt;Availability</td>
<td>
<ul>
<li>
<p>In Acumatica, If &quot;Set as Available (Don&rsquo;t Track Qty)&quot; -&gt; In WooCom Inventory tab-&gt; Manage Stock Boolean = False AND In Inventory tab-&gt; Stock Status dropdown = In Stock<br />[Default value = in stock]</p></li></ul></td>
<td>stock_status</td>
<td>instock</td>
<td colspan="1">Product-&gt; Inventory</td></tr>
<tr>
<td><s>Allow negative quantity</s></td>
<td colspan="1"><s>Stock Items&gt;General Settings&gt;Item Class&gt;General Settings&gt;AllowNegativequantity</s></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td><s>NegQty</s></td>
<td colspan="1">&nbsp;</td>
<td>&nbsp;</td>
<td>
<ul>
<li><s>If &quot;Allow Negative Quantity&quot; = False -&gt; Allow Back orders dropdown = No</s></li>
<li><s>If &quot;Allow Negative Quantity&quot; = True -&gt; Allow Back orders dropdown = Yes</s></li></ul></td>
<td><s>backorders</s></td>
<td><s>no</s></td>
<td colspan="1">&nbsp;</td></tr>
<tr>
<td>Weight</td>
<td colspan="1"><span>Stock Items&gt;Packaging &gt; Dimensions section</span></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td>BaseItemWeight</td>
<td colspan="1">InventoryItem</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>weight</td>
<td>&nbsp;</td>
<td colspan="1"><span>Product-&gt; Shipping</span></td></tr>
<tr>
<td><s>InventoryID</s></td>
<td colspan="1"><s>Stock Items&gt;Related Items&nbsp;</s></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td><s>INRelatedInventory</s></td>
<td colspan="1">&nbsp;</td>
<td><s><span>Stock Items&gt;InventoryID</span></s></td>
<td><s>In Related Items, Filter to Relations=Up-Sell</s></td>
<td><s>upsell_ids ****</s></td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td></tr>
<tr>
<td><s>InventoryID</s></td>
<td colspan="1"><s>Stock Items&gt;Related Items&nbsp;</s></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td><s>INRelatedInventory</s></td>
<td colspan="1">&nbsp;</td>
<td><s><span>Stock Items&gt;InventoryID</span></s></td>
<td><s>In Related Items, Filter to Relations=Cross-Sell</s></td>
<td><s>cross_sell_ids</s></td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td></tr>
<tr>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td>
<td>&nbsp;</td>
<td>
<p>Sales categories should sync beforehand, otherwise <strong><em>Uncategorized </em></strong>will pick from WooCommerce side.</p>
<p><strong><em> Inventory configuration default value can be setup </em></strong></p></td>
<td>categories</td>
<td>&nbsp;</td>
<td colspan="1"><span>Product-&gt; Product Categories</span></td></tr>
<tr>
<td>Search Keywords</td>
<td colspan="1"><span>Stock Items&gt;Ecommerce</span></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td>SearchKeywords</td>
<td colspan="1">InventoryItem</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>tags</td>
<td>&nbsp;</td>
<td colspan="1"><span>Product-&gt; Product tags</span></td></tr>
<tr>
<td><s>URL (Image)</s></td>
<td colspan="1"><s><span>Stock Items&gt;Ecommerce</span></s></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td><s>Media URLs</s></td>
<td colspan="1"><s>InventoryItem</s></td>
<td>&nbsp;</td>
<td><em>{Will be handled in M3}</em></td>
<td><s>images</s></td>
<td>&nbsp;</td>
<td colspan="1"><s><span>Product-&gt; Product image</span></s></td></tr>
<tr>
<td><s>InventoryID</s></td>
<td colspan="1"><s>Stock Items&gt;Related Items&nbsp;</s></td>
<td colspan="1" style="text-align: center;">&nbsp;</td>
<td><s>INRelatedInventory</s></td>
<td colspan="1">&nbsp;</td>
<td>&nbsp;</td>
<td><s>In Related Items, Filter to Relations=Related</s></td>
<td><s>grouped_products</s></td>
<td>&nbsp;</td>
<td colspan="1">&nbsp;</td></tr></tbody></table>
<p><s>Stock Items&gt;Related Items&nbsp;</s></p>
<p>**** Since the related Items concept will be changed in 2021r2, that has not considered in this mapping.</p>
<p>&nbsp;</p>
<p><span style="font-size: 20.0px;">Acumatica Stock Item and Item Type mapping with Woo Commerce Product type</span></p>
<p><span style="font-size: 20.0px;">&nbsp;</span>In WooCommerce four product types are using. In Acumatica those product types will be mapped as follows, in M1 only Product type = &quot;Simple Products&quot; will be exported.&nbsp;</p>
<table>
<tbody>
<tr>
<td class="highlight-grey" data-highlight-colour="grey">
<p><strong>Acumatica</strong></p></td>
<td class="highlight-grey" data-highlight-colour="grey">
<p><strong>WooCommerce Product type**</strong></p></td></tr>
<tr>
<td>
<p>In the Item class, &ldquo;Stock item&rdquo; = True and &ldquo;Item type&rdquo; = Finished Good</p></td>
<td>
<p>Simple Product</p></td></tr>
<tr>
<td>
<p><s>In the Item class, &ldquo;Stock item&rdquo; = True and &ldquo;Item type&rdquo; = Component Part</s></p></td>
<td>
<p><s>Grouped Product</s></p></td></tr>
<tr>
<td>
<p><s>In the Item class, &ldquo;Stock item&rdquo; = True and &ldquo;Item type&rdquo; = Subassembly</s></p></td>
<td>
<p><s>External/Affiliate Product</s></p></td></tr>
<tr>
<td>
<p><s>Template Item</s></p></td>
<td>
<p><s>Variable Product</s></p></td></tr></tbody></table>
<p>** In Acumatica Item Class, if &ldquo;Stock Item&rdquo; Boolean = False, those products will be mapped as &ldquo;Virtual&rdquo; = true, in WooCommerce.</p>
<p>&nbsp;</p>
<h2>Acumatica Item Status mapping with WooCommerce Item Status</h2>
<p>In milestone 1, Product status will be handled as follows,</p>
<table>
<tbody>
<tr>
<td class="highlight-grey" data-highlight-colour="grey">
<p><strong>Acumatica </strong></p></td>
<td class="highlight-grey" data-highlight-colour="grey">
<p><strong>WooCommerce Item Status</strong></p></td></tr>
<tr>
<td>
<p>Item Status = &ldquo;Active&rdquo;</p></td>
<td>
<p>Status = &ldquo;Published&rdquo;</p></td></tr>
<tr>
<td>
<p>Item Status = &ldquo;Inactive&rdquo;/ &ldquo;No Sale&rdquo;/ &ldquo;No Purchases&rdquo;/ &ldquo;No Request&rdquo;/ &ldquo;Marked for deletion&rdquo;</p></td>
<td>
<p>Status = &ldquo;Draft&rdquo;</p></td></tr></tbody></table>
