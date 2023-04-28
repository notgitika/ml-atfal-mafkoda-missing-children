# Documentation 

### Steps to reproduce code
1. `pip install -r requirements.txt` in a new virtual environment
2. `git clone`:

- https://github.com/eladrich/pixel2style2pixel
- https://github.com/AbuAbdULLAH-MuhammadAli/FaceAgingStyleGANs

3. From https://github.com/davisking/dlib-models download the models (you may have to change the paths in the code):

- mmod_human_face_detector.dat (use to detect face)
- shape_predictor_68_face_landmarks.dat (use to detect face)

4. From https://drive.google.com/file/d/1pJ_T-V1dpb1ewoEra1TGSWl5e6H7M4NN/view download:

- RRDB_ESRGAN_x4.pth (use to enhance image)

*if running from the BU SCC, ensure that the modules python 3.8.10, cuda 11.3, and gcc 9.3.0 are loaded prior to running interactive sessions.







### Known Issues:
1. There is a current issue after importing keras_vggface. You will need to make the change:

`from keras.engine.topology import get_source_inputs`

to

`from keras.utils.layer_utils import get_source_inputs` in `keras_vggface/models.py`.

### Citations 
PSP
```
@InProceedings{richardson2021encoding,
      author = {Richardson, Elad and Alaluf, Yuval and Patashnik, Or and Nitzan, Yotam and Azar, Yaniv and Shapiro, Stav and Cohen-Or, Daniel},
      title = {Encoding in Style: a StyleGAN Encoder for Image-to-Image Translation},
      booktitle = {IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
      month = {June},
      year = {2021}
}
```

2. When running the Facial Recognition notebook, a pickle file will be created with the embedding vectors of each image after running the FR once. This should take a little over an hour to do. If new images are added, you must delete the pickle file and rerun the FR notebook to create new embeddings, there is currently no way to append the pickle file with the new embeddings. 


FaceAgingGAN
```
@inproceedings{orel2020lifespan,
  title={Lifespan Age Transformation Synthesis},
  author={Or-El, Roy
          and Sengupta, Soumyadip
          and Fried, Ohad
          and Shechtman, Eli
          and Kemelmacher-Shlizerman, Ira},
  booktitle={Proceedings of the European Conference on Computer Vision (ECCV)},
  year={2020}
}
```



