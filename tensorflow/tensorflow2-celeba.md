# Can't Download CelebA from Google Drive

```python
dataset = tfds.load(
              name=data_type, # celeb_a
              split=split, 
              data_dir=data_dir, 
              download=True,
              try_gcs=False, 
              with_info=False, 
              as_supervised=False, 
              shuffle_files=shuffle
          )
```

## Issue

By setting `download=True`, it should automaically download celeb_a from google drive, but it fails for checksumerror.

## Solution

Manually download celeba from [google drive](https://drive.google.com/drive/folders/0B7EVK8r0v71pOC0wOVZlQnFfaGs?resourcekey=0-pEjrQoTrlbjZJO2UL8K_WQ).

Put it in the space as following hierarchy

```python
-- ./data/
-- -- downloads/
-- -- -- manual/
-- -- -- -- identity_CelebA.txt
-- -- -- -- img_align_celeba.zip
-- -- -- -- list_attr_celeba.txt
-- -- -- -- list_bbox_celeba.txt
-- -- -- -- list_eval_partition.txt
-- -- -- -- list_landmarks_align_celeba.txt
-- -- -- -- list_landmarks_celeba.txt
```

Pass `data_dir='./data/'`, then it will automatically prepare.