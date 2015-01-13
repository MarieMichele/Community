 public static class List_clsErrorDescription
    {
        public static string ListToString(this IList<clsErrorDescription> obj)
        {
            string a_Res = "";
            foreach (clsErrorDescription a_Err in obj)
            {
                if (a_Res != "")
                    a_Res += ", ";
                a_Res += a_Err.Description;
            }
            return a_Res;
        }
    }
