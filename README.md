# Nextjs_E-commerce-website

Online link: 
e-commerce website with Next.js using Prisma and MongoDB for database management,Tailwind CSS and DaisyUI for UI



**Landing page**

  The landing page of the website displays the products,in the order that they were introduced in the database,from newest to oldest. Information about the newest item introduced is wrapped in divs with the "hero" and "hero-content" styling and will be displayed above all the others on top of the page.The rest of the products are displayed using a <ProductCard> component that displays the product name,a new tag,if the product is no older than 7 days,the product description and the price. The price is also wrapped in a PriceTag component that formats the value introduced in the database by dividing the number written in front of it and adding the appropiate currency symbol: €,in this case. The last item displayed on the page is the PaginationBar,this will only be displayed if the number of total pages is >1 whereas the number of total pages is calculated by dividing the number of total items minus the number of hero styled items that we want to display (in this case 1),and dividing it by the number of items that we want to display on a page.

**Pagination**
  Navigation through the different pages is done using the <NavigationBar> component,based on the number of items,this component will calculate a minimum and maximum page number to be displayed and will render a number of Highest_page_number_to_be_displayed-Lowest_page_number_to_be_displayed JSX.Element numberedPageItems elements,the link corresponding to the 
  

