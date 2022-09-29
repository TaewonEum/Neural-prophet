# Neural-prophet

산자부 태양광 보급사업 예산사업 효율화 및 연계활용을 위한 Pilot분석 코드입니다.

데이터 출처: Dacon 동서발전 태양광 발전량 예측 AI 경진대회

데이터분석 환경: Jupyter lab

사용모델: Neural Prophet 시계열 모델

발전량 예측은 대표적인 시계열 분석에 해당하기 때문에 기존의 시계열 분석에서 Neural Network 알고리즘은 반영한 Neural Prophet 모델 사용

import pandas as pd
import numpy as np
import csv
import os
import os.path
import matplotlib.pyplot as plt
import warnings
import seaborn as sns
import scipy.stats as ss
from scipy.stats import anderson
from datetime import timedelta, datetime
from dateutil import parser
from tqdm import tqdm
import copy
from statsmodels.tsa.arima.model import ARIMA
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from neuralprophet import NeuralProphet #Neuralprophet 설치
import warnings
import datetime
warnings.filterwarnings("ignore")
from glob import glob
import plotly.express as px
from torch.utils.tensorboard import SummaryWriter
