# Nextjs_E-commerce-website

Online link: 

e-commerce website with Next.js using Prisma and MongoDB for database management,Tailwind CSS and DaisyUI for UI



**Landing page**

  The landing page of the website displays the products,in the order that they were introduced in the database,from newest to oldest. Information about the newest item introduced is wrapped in divs with the "hero" and "hero-content" styling and will be displayed above all the others on top of the page.The rest of the products are displayed using a <ProductCard> component that displays the product name,a new tag,if the product is no older than 7 days,the product description and the price. The price is also wrapped in a PriceTag component that formats the value introduced in the database by dividing the number written in front of it and adding the appropiate currency symbol: €,in this case. The last item displayed on the page is the PaginationBar,this will only be displayed if the number of total pages is >1 whereas the number of total pages is calculated by dividing the number of total items minus the number of hero styled items that we want to display (in this case 1),and dividing it by the number of items that we want to display on a page.

**Product details**
  The ProductCard component is wrapped in a link that takes the user to the product detail page,if the id of the product in the product card is found,otherwise,the user will be redirected to the not found page.Upon success, the user is shown a page containing the product image,name,price,description and an "Add To Cart" button.

**Adding a product**
  In the current state of the project any user can add a product to the website,however,they must be logged in via Google account using the UserMenuButton component,found to the right of the NavBar.Once logged in,the user can get to the add product page by adding "add-product" to the URL.To add a new product the user will be prompted to fill out a form containing the following fields: name, description,image url and price,leaving any of these fields open will throw a "Missing required fields" error,also, image URLs can only be imported from "unsplash.com" because that is the only image hosting site that is given permission in the next.config file for now.

**Pagination**

  Navigation through the different pages is done using the <NavigationBar> component,based on the number of items in the database and the current page,this component will calculate a minimum and maximum page number to be displayed and will render a number of Highest_page_number_to_be_displayed-Lowest_page_number_to_be_displayed JSX.Element numberedPageItems elements,it will also check what the current page number is and disable the link corresponding to that page number.When a page is clicked the "?page="+the page is added to the URL address,so,changing the page number directly in the URL address will not work.

**Search function**

     The searchbar is located in the NavBar component at the top of the screen,this will execute the SearchPage function,in the database 

**Data source**

     The data source for this project is a MongoDB database,through a Prisma ORM,and contains information about various objects:products,cartitems(stores the productid and quantity of a product contained within a cart),carts ,user accounts,sessions,etc.
  

