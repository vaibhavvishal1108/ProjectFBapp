# Facebook Photo Review Guide

## Purpose:

We intend to build a Facebook app "FB Photo Analyst", wherein Facebook users have the option of running an analysis on their photos, retrieved from their Facebook account. The Google Vision API is used to detect "labels" on selected photos. Based on those labels, our application will provide a brief analysis report to user, which will give an insight on the likes and dislikes from his/her followers/friends. It will enable user to take and upload more photos related to the labels detected and avoid those which got less/minimum likes. So, the user can post the photos according to our app analysis and gain more reach, likes and followers on Facebook.

## Highlights:

Different users will have different analyses based on the type of photos they have with more likes or reach. Every user will get a detailed analysis of what their followers or friends liked photos have in them.
 
## GUI Mock-up Screens:

User has to select date range for photos to be analyzed by our application

![select date](https://user-images.githubusercontent.com/50223742/99532919-ea05aa00-2959-11eb-89bc-3dfb76d8372a.jpg)

**User given option to select from "max" or "min" liked photos**

![selection option](https://user-images.githubusercontent.com/50223742/99530690-7f9f3a80-2956-11eb-85cb-87a7b9ac8f63.jpg)

### MAX linked photo
![](https://raw.githubusercontent.com/dievlone/picBed/master/20201113001121.jpg)

### MIN linked photo
![](https://raw.githubusercontent.com/dievlone/picBed/master/20201113001120.jpg)

**Now, if User selects "Min" liked photo, for ex: the one with 13 likes as shown above, that photo will be fed to Google Vision API**

**Google Vision API will detect the labels on the photo as shown here**
![traffic vision API](https://user-images.githubusercontent.com/50223742/99531285-5af79280-2957-11eb-8edc-ecb1150e1f55.png)


![20201113001121](https://user-images.githubusercontent.com/50223742/99535636-060b4a80-295e-11eb-976f-c117d672bb5e.jpg)

## Sample datastore:
```json
{
	"photo_id": "954839471708381",
	"image_url": "https://scontent-sjc3-1.xx.fbcdn.net/v/t1.0-9/125178955_954839471708381_1839396585296945290_n.jpg?_nc_cat=101&ccb=2&_nc_sid=8bfeb9&_nc_ohc=v6fdrkNpNRsAX9CJ0tY&_nc_ht=scontent-sjc3-1.xx&oh=dc8b43b9b09dfb3d2c46224af806fb01&oe=5FD94382",
	"likes": "13"
}
```

As per the date range selected, all the users photos in that date range will be stored in our Google datastore.

![datastore](https://user-images.githubusercontent.com/50223742/99534667-a06a8e80-295c-11eb-93ee-af73d740445f.png)

## App Requirements:

* Users should be able to login using their Facebook ID.
* Users must allow the App to access their FB photos.

## App User's Work-flow:

1. To access this Facebook App, the user must give access to their photos and likes to get a review on their image posts or photos.

2. Now the user will choose the date 

3. Within the date range provided, all the user photos will be fetched by our application and saved in our Google datastore along with their respective likes.

4. Since application has access to likes of photos, the maximum and minimum liked photo for the selected date range will displayed to user 

 
5. User will have to now choose the type of photo he/she wants to be reviewed, it can be a maximum liked photo or a minimum liked 
    photo.   

6. For ex: if user chooses a maximum liked photo, it will be sent to google vision API for analyzing the labels present in that photo.

7. On the application screen, the user will now be displayed with labels that the user's friends liked the most in that particular photo, ex: sunset, trees, beach

8. Our application would indicate and inform the user to upload more photos having sunset, trees etc as per the analysis to get more likes and subsequently get ore reach in social network.

9. As for newness is concerned, every time the user will get new and fresh photo selection options based on the date range selected.

