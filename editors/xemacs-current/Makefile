# $NetBSD: Makefile,v 1.93 2017/11/17 15:09:34 hauke Exp $

PKGNAME=	${DISTNAME}
COMMENT=	*BETA* XEmacs text editor version ${PKGVERSION_NOREV}

# extra options for x11 support, not for sharing with xemacs-current-nox11

PKG_SUPPORTED_OPTIONS+=		x11 xft xface
PKG_SUGGESTED_OPTIONS+=		x11

.include "options.mk"
.include "Makefile.common"
.include "../../mk/bsd.pkg.mk"
