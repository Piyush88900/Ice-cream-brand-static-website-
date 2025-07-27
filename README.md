
## 🖼️ Website Features

- Clean, responsive layout
- Simple design using HTML and inline CSS
- Ice cream flavors with images
- Hosted via Amazon S3 as a public static website

## 🚀 Hosting on AWS S3 (Steps)

1. Create an S3 bucket (e.g., `icecream-delight`).
2. Enable static website hosting.
3. Upload `index.html` and the image files (`chocolate.jpg`, `vanilla.jpg`).
4. Set bucket policy to allow public read access:
   ```json
   {
     "Version": "2012-10-17",
     "Statement": [
       {
         "Sid": "PublicReadGetObject",
         "Effect": "Allow",
         "Principal": "*",
         "Action": "s3:GetObject",
         "Resource": "arn:aws:s3:::your-bucket-name/*"
       }
     ]
   }
