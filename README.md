## Edge Case Handling
1. Invalid polygons skipped (`len(poly) < 6`).
2. Annotations without segmentation data are ignored.
3. Incorrect category IDs are filtered via category_map.
4. Overlapping masks are handled by order of appearance.
5. Each polygon is drawn safely using `skimage.draw.polygon`.
6. Mask values are consistent via integer category remapping.
7. Incomplete or unreadable images are skipped.
8. All images are checked for file existence before mask creation.
9. Masks are saved with the same filenames as the original image.
10. Images without any annotations result in all-zero masks.
