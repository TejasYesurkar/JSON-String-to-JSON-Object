# JSON-String-to-JSON-Object

String ==>  {"result":[{"a":"1","b":"2"}]}

                                    Dim json As String = RawData
                                    Dim jsonObject As Newtonsoft.Json.Linq.JObject = Newtonsoft.Json.Linq.JObject.Parse(json)
                                    'MsgBox(jsonObject.SelectToken("PartyNameList")(0)("RequestType"))
                                    Dim jsonArray As JArray = jsonObject("result")(0)("RequestType")

                                    For Each item As JObject In jsonArray
                                        RichTextBox1.Text = item.SelectToken("a").ToString
                                    Next
