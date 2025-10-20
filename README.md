# EasyCode

Php Website that provides tutorials for Basic Html,Css,Js

Checkout this project running : [HERE](http://easycode_sid.comxa.com)




uploadFeed(file: File | null, requestDto: any): Observable<any> {
  const formData = new FormData();

  // Add file only if present
  if (file) {
    formData.append('file', file);
  }

  // Add JSON as a Blob, with proper content type
  formData.append('request', new Blob([JSON.stringify(requestDto)], { type: 'application/json' }));

  return this.http.post('/api/bulk-transactions/upload', formData);
}
