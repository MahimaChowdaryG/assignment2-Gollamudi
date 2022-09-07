# assignment2-Gollamudi
# Mahima Chowdary Gollamudi
### Salar Jung Museum

The must see exhibits in Salar Jung Museum are **A wardrobe of Tipu Sultan**, **daggers of Shah Jahan and Jehangir**, **Aurangzeb's sword**, and a **painting of Raja Ram Mohan Roy**.

---------------------------------------------------

### Directions to the museum from the nearest airport and places to vist nearby

The closest airport is the Rajiv Gandhi International Airport.Directions from the airport to the museum are
1. Take a straight road that takes you to the Tank Bund.
2. Take a left turn at the Tank bund and travel for 20 miles till you reach the statue of Budha.
3. Take a U turn now and go straight for 2 miles.
4. Take a right here and you find the Salar Jung Museum to your left.

Other places to visit surrounding the museum:
* Chowmahalla Palace
* Charminar
* Mecca Masjid
* Purani Haveli

[Click here to know AboutMe](./AboutMe.md)

----------------------------------------------------------------

### Recommended cities to visit

My recommendation for the list of cities to vist along with their important locations and amount of time to spend are

| City Name    | Visit Spot                  | Time to spend   |
| ------------ | --------------------------- | --------------- |
| Vijayawada   | KanakaDurga Temple          | 2 hours         |
| Hyderabad    | NTR Park                    | 5 hours         |
| Vizag        | Beach                       | 1 hours         |
| Goa          | Titos lane                  | 6 hours         |

-------------------------------------------------------------------

### Quotes

> You will face many defeats in life, but never let yourself be defeated. - *Stephen Chbosky*

> The greatest glory in living lies not in never falling, but in rising every time we fall.  - *John Steinbeck*

---------------------------------------------------------------------

### Code Snippets

> I have custom post types called clients, need to display 5 clients per page with pagination. The page what i have is page-clients.php.I have used the wp_pagenavi plugin.I get a perfect navigation list 1,2,3 etc but on clicking them takes me to page not found

Refer to the following link: <https://stackoverflow.com/questions/15524195/wordpress-custom-post-page-with-pagination>

```
<?php 
  $temp = $wp_query; 
  $wp_query = null; 
  $wp_query = new WP_Query(); 
  $wp_query->query('showposts=6&post_type=news'.'&paged='.$paged); 

  while ($wp_query->have_posts()) : $wp_query->the_post(); 
?>

  <!-- LOOP: Usual Post Template Stuff Here-->

<?php endwhile; ?>

<nav>
    <?php previous_posts_link('&laquo; Newer') ?>
    <?php next_posts_link('Older &raquo;') ?>
</nav>

<?php 
  $wp_query = null; 
  $wp_query = $temp;  // Reset
?>
```

Source: <https://css-tricks.com/snippets/wordpress/paginate-custom-post-types/>