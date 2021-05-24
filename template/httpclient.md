# HttpClient





```typescript

const instance = axios.create({
  baseURL: ''
});

instance.interceptors.request.use(res => {
  res.headers = {
      // TODO
    authorization: ''
    'Content-Type': 'application/json',
  };
  return res;
});

instance.interceptors.response.use(
  res => {
    // TODO
    return res;
  },
);

const HttpClient = {
  get<T>(url: string, config?: AxiosRequestConfig): Promise<AxiosResponse<T>> {
    return instance.get(url, config);
  },

  post<T = any>(url: string, data?: any, config?: AxiosRequestConfig) {
    return instance.post(url, data, config) as Promise<T>;
  },

  delete(url: string, config?: AxiosRequestConfig) {
    return instance.delete(url, config);
  },

  options(url: string, config?: AxiosRequestConfig) {
    return instance.options(url, config);
  },

  put<T>(url: string, data: any, config?: AxiosRequestConfig): Promise<AxiosResponse<T>> {
    return instance.put(url, data, config);
  },

  patch<T>(url: string, data: any, config?: AxiosRequestConfig): Promise<AxiosResponse<T>> {
    return instance.patch(url, data, config);
  },

  head(url: string, config?: AxiosRequestConfig) {
    return instance.patch(url, config);
  },
};

export default HttpClient;

```

